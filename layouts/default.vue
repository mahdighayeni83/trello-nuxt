<template>
  <v-app light>
    <v-main>
      <v-container fluid>
        <v-row class="main-navbar justify-space-between">
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <svg width="24" height="24" role="presentation"
                   focusable="false" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M4 5C4 4.44772 4.44772 4 5 4H7C7.55228 4 8 4.44772 8 5V7C8 7.55228 7.55228 8 7 8H5C4.44772 8 4 7.55228 4 7V5ZM4 11C4 10.4477 4.44772 10 5 10H7C7.55228 10 8 10.4477 8 11V13C8 13.5523 7.55228 14 7 14H5C4.44772 14 4 13.5523 4 13V11ZM11 4C10.4477 4 10 4.44772 10 5V7C10 7.55228 10.4477 8 11 8H13C13.5523 8 14 7.55228 14 7V5C14 4.44772 13.5523 4 13 4H11ZM10 11C10 10.4477 10.4477 10 11 10H13C13.5523 10 14 10.4477 14 11V13C14 13.5523 13.5523 14 13 14H11C10.4477 14 10 13.5523 10 13V11ZM17 4C16.4477 4 16 4.44772 16 5V7C16 7.55228 16.4477 8 17 8H19C19.5523 8 20 7.55228 20 7V5C20 4.44772 19.5523 4 19 4H17ZM16 11C16 10.4477 16.4477 10 17 10H19C19.5523 10 20 10.4477 20 11V13C20 13.5523 19.5523 14 19 14H17C16.4477 14 16 13.5523 16 13V11ZM5 16C4.44772 16 4 16.4477 4 17V19C4 19.5523 4.44772 20 5 20H7C7.55228 20 8 19.5523 8 19V17C8 16.4477 7.55228 16 7 16H5ZM10 17C10 16.4477 10.4477 16 11 16H13C13.5523 16 14 16.4477 14 17V19C14 19.5523 13.5523 20 13 20H11C10.4477 20 10 19.5523 10 19V17ZM17 16C16.4477 16 16 16.4477 16 17V19C16 19.5523 16.4477 20 17 20H19C19.5523 20 20 19.5523 20 19V17C20 16.4477 19.5523 16 19 16H17Z" fill="currentColor"></path>
              </svg>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <svg width="24" height="24" role="presentation"
                   focusable="false" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M3.58579 10.4142C3.21071 10.7893 3 11.298 3 11.8284V19C3 20.1045 3.89543 21 5 21H10C10.5523 21 11 20.5523 11 20V14H13V20C13 20.5523 13.4477 21 14 21H19C20.1046 21 21 20.1045 21 19V11.8284C21 11.298 20.7893 10.7893 20.4142 10.4142L12.7071 2.70708C12.3166 2.31655 11.6834 2.31655 11.2929 2.70708L3.58579 10.4142ZM13 12C14.1046 12 15 12.8954 15 14V19H19V11.8284L12 4.8284L5 11.8284V19H9V14C9 12.8954 9.89543 12 11 12H13Z" fill="currentColor"></path>
              </svg>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded d-flex">
              <svg width="24" height="24" role="presentation" focusable="false"
                   viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M3 5C3 3.89543 3.89543 3 5 3H19C20.1046 3 21 3.89543 21 5V19C21 20.1046 20.1046 21 19 21H5C3.89543 21 3 20.1046 3 19V5ZM5 6C5 5.44772 5.44772 5 6 5H10C10.5523 5 11 5.44772 11 6V16C11 16.5523 10.5523 17 10 17H6C5.44772 17 5 16.5523 5 16V6ZM14 5C13.4477 5 13 5.44772 13 6V12C13 12.5523 13.4477 13 14 13H18C18.5523 13 19 12.5523 19 12V6C19 5.44772 18.5523 5 18 5H14Z" fill="currentColor"></path>
              </svg>
              <span class="px-1">Boards</span>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <v-dialog
                transition="dialog-top-transition"
                max-width="600"
              >
                <template v-slot:activator="{ on }">
                  <div
                    class="input-search-navbar d-flex justify-end"
                    v-on="on"
                  >
                    <span class="px-2">
                      <svg width="24" height="24" role="presentation" focusable="false"
                           viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M10.5 18C6.35786 18 3 14.6421 3 10.5C3 6.35786 6.35786 3 10.5 3C14.6421 3 18 6.35786 18 10.5C18 12.2269 17.4164 13.8175 16.4356 15.0852L20.3769 19.0953C20.764 19.4892 20.7586 20.1223 20.3647 20.5095C19.9708 20.8966 19.3376 20.8911 18.9505 20.4972L15.0129 16.4909C13.7572 17.4383 12.1942 18 10.5 18ZM16 10.5C16 13.5376 13.5376 16 10.5 16C7.46243 16 5 13.5376 5 10.5C5 7.46243 7.46243 5 10.5 5C13.5376 5 16 7.46243 16 10.5Z" fill="currentColor"></path>
                      </svg>
                    </span>
                  </div>
                </template>
                <template v-slot:default="dialog">
                  <v-card class="modal-search">
                    <v-toolbar
                      color="white"
                    >
                      <template>
                        <div class="input-search-in-modal">
                          <v-text-field
                            placeholder="Search"
                            hide-details="auto"
                          ></v-text-field>
                        </div>
                      </template>
                    </v-toolbar>
                    <v-card-text>
                      <div class="text-h2 pa-12 text-center">Search : )</div>
                    </v-card-text>
                    <v-card-actions class="justify-end">
<!--                      <v-btn class="rounded-circle text-lowercase"-->
<!--                        text-->
<!--                        @click="dialog.value = false"-->
<!--                      >bk!</v-btn>-->
                    </v-card-actions>
                  </v-card>
                </template>
              </v-dialog>
            </div>
          </v-col>
          <v-col cols="" class="pa-1">
            <div class="main-navbar-item pa-1 rounded not-background d-flex justify-center">
              <div class="site-name-navbar">Trello</div>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <svg width="24" height="24" role="presentation" focusable="false"
                   viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 3C11.4477 3 11 3.44772 11 4V11L4 11C3.44772 11 3 11.4477 3 12C3 12.5523 3.44772 13 4 13H11V20C11 20.5523 11.4477 21 12 21C12.5523 21 13 20.5523 13 20V13H20C20.5523 13 21 12.5523 21 12C21 11.4477 20.5523 11 20 11L13 11V4C13 3.44772 12.5523 3 12 3Z" fill="currentColor"></path>
              </svg>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <svg width="24" height="24" role="presentation" focusable="false"
                   viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12 20C16.4183 20 20 16.4183 20 12C20 7.58172 16.4183 4 12 4C7.58172 4 4 7.58172 4 12C4 16.4183 7.58172 20 12 20ZM12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" fill="currentColor"></path><path d="M11 11C11 10.4477 11.4477 10 12 10C12.5523 10 13 10.4477 13 11V16C13 16.5523 12.5523 17 12 17C11.4477 17 11 16.5523 11 16V11Z" fill="currentColor"></path><path d="M13 8C13 8.55228 12.5523 9 12 9C11.4477 9 11 8.55228 11 8C11 7.44772 11.4477 7 12 7C12.5523 7 13 7.44772 13 8Z" fill="currentColor"></path>
              </svg>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <svg width="24" height="24" role="presentation" focusable="false"
                   viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C11.4477 2 11 2.44772 11 3V3.078C10.2728 3.19668 9.65318 3.44603 9.1328 3.79295C8.39456 4.28511 7.91489 4.93416 7.60557 5.55279C7.29822 6.1675 7.14952 6.77011 7.07611 7.2106C7.039 7.43322 7.02007 7.62092 7.01035 7.75688C7.00549 7.82503 7.0029 7.88067 7.00153 7.92176C7.00085 7.94232 7.00046 7.95929 7.00025 7.9724L7.00005 7.98916L7.00001 7.99533L7 7.99786L7 7.99898C7 7.9995 7 8 8 8H7V11.723L4.14251 16.4855C3.95715 16.7944 3.95229 17.1792 4.1298 17.4927C4.30731 17.8062 4.63973 18 5 18H19C19.3603 18 19.6927 17.8062 19.8702 17.4927C20.0477 17.1792 20.0429 16.7944 19.8575 16.4855L17 11.723V8H16C17 8 17 7.9995 17 7.99898L17 7.99786L17 7.99533L17 7.98916L16.9997 7.9724C16.9995 7.95929 16.9992 7.94232 16.9985 7.92176C16.9971 7.88067 16.9945 7.82503 16.9896 7.75688C16.9799 7.62092 16.961 7.43322 16.9239 7.2106C16.8505 6.77011 16.7018 6.1675 16.3944 5.55279C16.0851 4.93416 15.6054 4.28511 14.8672 3.79295C14.3468 3.44603 13.7272 3.19668 13 3.078V3C13 2.44772 12.5523 2 12 2ZM9.00042 7.98839L9 8.00435V12C9 12.1812 8.95074 12.3591 8.85749 12.5145L6.76619 16H17.2338L15.1425 12.5145C15.0493 12.3591 15 12.1812 15 12V8.00436L14.9996 7.98839C14.999 7.97089 14.9977 7.9406 14.9947 7.89937C14.9888 7.81658 14.9765 7.69178 14.9511 7.5394C14.8995 7.22989 14.7982 6.8325 14.6056 6.44721C14.4149 6.06584 14.1446 5.71489 13.7578 5.45705C13.3773 5.20338 12.825 5 12 5C11.175 5 10.6227 5.20338 10.2422 5.45705C9.85544 5.71489 9.58511 6.06584 9.39443 6.44721C9.20178 6.8325 9.10048 7.22989 9.04889 7.5394C9.0235 7.69178 9.01118 7.81658 9.00527 7.89937C9.00233 7.9406 9.001 7.97089 9.00042 7.98839ZM14 19C14 20.1046 13.1046 21 12 21C10.8954 21 10 20.1046 10 19H14Z" fill="currentColor"></path>
              </svg>
            </div>
          </v-col>
          <v-col cols="auto" class="pa-1">
            <div class="main-navbar-item pa-1 rounded">
              <svg width="24" height="24" role="presentation" focusable="false"
                   viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12.0254 3C9.25613 3 7.01123 5.23858 7.01123 8C7.01123 10.7614 9.25613 13 12.0254 13C14.7946 13 17.0395 10.7614 17.0395 8C17.0395 5.23858 14.7946 3 12.0254 3ZM9.01688 8C9.01688 9.65685 10.3638 11 12.0254 11C13.6869 11 15.0338 9.65685 15.0338 8C15.0338 6.34315 13.6869 5 12.0254 5C10.3638 5 9.01688 6.34315 9.01688 8Z" fill="currentColor"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M12.0254 11C16.7803 11 20.6765 14.6667 21.0254 19.3194C20.8721 20.2721 20.0439 21 19.0452 21H18.9741C18.9741 21 18.9741 21 18.9741 21L5.0767 21C5.07671 21 5.0767 21 5.0767 21L5.00562 21C4.00691 21 3.1787 20.2721 3.02539 19.3193C3.37428 14.6667 7.27038 11 12.0254 11ZM5.0767 19H18.9741C18.4875 15.6077 15.5618 13 12.0254 13C8.48892 13 5.56331 15.6077 5.0767 19ZM19.0451 19.9769V20.0231C19.0452 20.0154 19.0452 20.0077 19.0452 20C19.0452 19.9923 19.0452 19.9846 19.0451 19.9769Z" fill="currentColor"></path>
              </svg>
            </div>
          </v-col>
        </v-row>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      rules: [
        value => !!value || 'Required.',
        value => (value && value.length >= 3) || 'Min 3 characters',
      ],
    }
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: "Apercu";
  src: url("static/fonts/Apercu-Font/Apercu Medium.otf");
}
@font-face {
  font-family: "Apercu-italic";
  src: url("static/fonts/Apercu-Font/Apercu Medium italic.otf");
}
*{
  font-family: "Apercu";
}
.v-application {
  background: white !important;
  color: black !important;
}
.main-navbar {
  height: 40px;
  background-color: rgba(0, 0, 0, 0.12);
  color: white;
}
.main-navbar-item:not(.not-background) {
  min-width: 32px;
  max-height: 32px;
  background-color: rgba(0, 0, 0, 0.22);
}
.input-search-navbar{
  min-width: 200px;
  height: 24px;
  cursor: pointer;
  span{
    cursor: pointer;
  }
}
.site-name-navbar{
  font-family: "Apercu-italic";
  font-size: 1.1rem;
  color: #000;
}
.input-search-in-modal {
  width: 100%;
  margin-bottom: -10px;
  input{
    text-align: center;
  }
  input::placeholder{
    color: rgba(1, 94, 104, 0.53) !important;
  }
}
</style>
