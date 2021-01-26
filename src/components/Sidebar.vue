<template>
        <aside class="column is-2 is-narrow-mobile is-fullheight section is-hidden-mobile">
        <p class="menu-label is-hidden-touch">Navigation</p> <hr>
        <ul class="menu-list">
          <li>
            <a href="/Dashboard" class="">
              <span class="icon"><i class="fa fa-home"></i></span> Dashboard
            </a>
          </li>
          <li>
            <a href="/Advisory">
              <span class="icon"><i class="fa fa-table"></i></span> Advisory
            </a>
          </li>
          <li>
            <a href="/Recipients">
                <span class="icon"><i class="fa fa-link"></i></span> Recipients
            </a>
          </li>
            <li>
            <a href="/">
                <span class="icon"><i class="fa fa-link"></i></span> Logout
            </a>
            </li>
        </ul>
        
        <div class="card-forecast">
          <b-card> Forecast
              <hr>
              <div class="container forecast-index__header">
                <div class="weather-actions" layout="row center-justify">
                  <div class="icon-button icon-button--horizontal weather-actions__action weather-actions__action--location weather-actions__action weather-actions__action--location" layout="row center-left" data-tooltip="Set location" data-tooltip-position="right">
                    <svg class="icon icon--map-pin-line icon-button__icon">
                      <use xlink:href="/icons.svg#map-pin-line"></use>
                    </svg>
                    <div class="icon-button__label" self="size-x1">
                      <div>Santa Cruz</div>
                    </div>
                  </div>
                  <div self="size-x1"></div>
                  <div class="icon-button icon-button--horizontal weather-actions__action weather-actions__action--update weather-actions__action weather-actions__action--update" layout="row center-left" data-tooltip="Update" data-tooltip-position="left">
                    <svg class="icon icon--refresh-line icon-button__icon">
                      <use xlink:href="/icons.svg#refresh-line"></use>
                      </svg><!--v-if-->
                  </div>
                </div>
                
                <header class="forecast-index__summary" layout="column center-stretch">
                  <div class="forecast-summary">
                    <div layout="row center-justify">
                      <div>
                        <div class="forecast-summary__temp">29°C</div>
                        <div class="forecast-summary__feels-like"><small>Feels like 33°C</small></div>
                        <div class="forecast-summary__description"><small>Scattered clouds</small></div>
                      </div>
                    <div>
                      <img class="forecast-summary__figure" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMj
                      AwMC9zdmciIHZpZXdCb3g9IjAgMCA0OCA0OCIgd2lkdGg9Ijk2cHgiIGhlaWdodD0iOTZweCI+PGxpbmVhckdyYWRpZW50IGlkPSJlYXVWVFJJZ
                      UNXd1o2NUdPdEdvTWphIiB4MT0iNS43MDciIHgyPSIyMy43NjIiIHkxPSI3LjcwNyIgeTI9IjI1Ljc2MiIgZ3JhZGllbnRVbml0cz0idXNlclNw
                      YWNlT25Vc2UiPjxzdG9wIG9mZnNldD0iMCIgc3RvcC1jb2xvcj0iI2ZlZDEwMCIvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iI2UzNjA
                      wMSIvPjwvbGluZWFyR3JhZGllbnQ+PHBhdGggZmlsbD0idXJsKCNlYXVWVFJJZUNXd1o2NUdPdEdvTWphKSIgZD0iTTE2LDdDOS45MjUsNyw1LD
                      ExLjkyNSw1LDE4czQuOTI1LDExLDExLDExczExLTQuOTI1LDExLTExUzIyLjA3NSw3LDE2LDd6Ii8+PGxpbmVhckdyYWRpZW50IGlkPSJlYXVWV
                      FJJZUNXd1o2NUdPdEdvTWpiIiB4MT0iMjIuMzEzIiB4Mj0iMjYuNjE4IiB5MT0iMTYuMDc5IiB5Mj0iNDEuNDQ4IiBncmFkaWVudFVuaXRzPSJ1
                      c2VyU3BhY2VPblVzZSI+PHN0b3Agb2Zmc2V0PSIwIiBzdG9wLWNvbG9yPSIjZmNmY2ZjIi8+PHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSI
                      jYzNjOWNkIi8+PC9saW5lYXJHcmFkaWVudD48cGF0aCBmaWxsPSJ1cmwoI2VhdVZUUkllQ1d3WjY1R090R29NamIpIiBkPSJNMzUsMjFjLTAuMz
                      MxLDAtMC42NTcsMC4wMTgtMC45OCwwLjA0OUMzMS43NDEsMTcuOTksMjguMTA4LDE2LDI0LDE2CWMtNS43MTMsMC0xMC41MiwzLjgzNy0xMi4wM
                      TIsOS4wNzFDOC4wNDksMjUuNTY5LDUsMjguOTI1LDUsMzNjMCw0LjQxOCwzLjU4Miw4LDgsOGMxLjgxOCwwLDIwLjEwNywwLDIyLDBjNS41MjMs
                      MCwxMC00LjQ3NywxMC0xMAlDNDUsMjUuNDc3LDQwLjUyMywyMSwzNSwyMXoiLz48L3N2Zz4=" alt="scattered clouds">
                    </div>
                  </div>
                  
                  <div class="forecast-summary__last-updated"><small>Updated 2 minutes ago</small></div>
                </div>
              </header>
            </div>
          </b-card>
        </div>
        </aside>
</template>

<script>
export default {
    name: "Sidebar"
}
</script>

<style scoped>
    .menu-list a {
    border-radius: 2px;
    color: #4a4a4a;
    display: block;
    padding: .5em .75em;
    text-align: left;
    }

    .menu-label {
    color: #7a7a7a;
    font-size: .75em;
    letter-spacing: .1em;
    text-transform: uppercase;
    text-align: left;
}
</style>