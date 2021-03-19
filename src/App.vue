<template>
  <div id="ui-container">
    <div id="notifications">
      <Notification
        v-for="notif in activeNotifications"
        :key="notif"
        :type="notif.typeId"
        :content="notif.content"
      ></Notification>
    </div>
  </div>
</template>

<script>
import Notification from "./components/Notification.vue";

export default {
  name: "App",
  data() {
    return {
      activeNotifications: [
        {
          typeId: 0,
          fadeOutTime: 10000,
          content: {
            title: "Important",
            content: "this is an important notification!"
          }
        },
        {
          typeId: 1,
          fadeOutTime: 15000,
          content: {
            title: "Announcement",
            content: "This is in development!"
          }
        },
        {
          typeId: 2,
          fadeOutTime: 5000,
          content: {
            title: "Info",
            content: "some info lol"
          }
        },
        {
          typeId: 3,
          fadeOutTime: 7500,
          content: {
            title: "Success",
            content: "You succeeded in... something?"
          }
        },
        {
          typeId: 4,
          fadeOutTime: 10000,
          content: {
            title: "Failure",
            content: "Wellllll you screwed up apparently"
          }
        },
        {
          typeId: 5,
          fadeOutTime: 15000,
          content: {
            title: "Warning",
            content: "Something may go wrong if you do this!"
          }
        },
        {
          typeId: 6,
          fadeOutTime: 20000,
          content: {
            title: "Error",
            content: "Something went wrong!"
          }
        }
      ]
    };
  },
  components: {
    Notification
  }
};
</script>

<style lang="scss">
#ui-container {
  // sizes
  --scale: 1;
  --notification-width-scale: 1;
  --notification-height-scale: 1;
  --notification-gap-scale: 1;

  // theme color variables
  --bg-primary: #4a4a55;
  --bg-secondary: #232323;
  --color-primary: #23bf7c;
  --color-secondary: #299465;
  --text-primary: #f7f7f7;
  --text-secondary: #dfdfdf;

  // message type vars
  --color-important: #ff4433;
  --opacity-important: 0.95;

  --color-announcement: #ff4433;
  --opacity-announcement: 0.8;

  --color-info: #23bf7c;
  --opacity-info: 0.5;

  --color-success: #33cc33;
  --opacity-success: 0.75;

  --color-failure: #bb4433;
  --opacity-failure: 0.75;

  --color-warning: #ffee00;
  --opacity-warning: 0.9;

  --color-error: #ff0000;
  --opacity-error: 0.9;

  #notifications {
    display: grid;
    padding: calc(2vh * var(--notification-gap-scale));
    gap: calc(2vh * var(--notification-gap-scale));
  }
}
html, body {
  margin: 0;
  padding: 0;
}
* {
  box-sizing: border-box;
}
</style>
