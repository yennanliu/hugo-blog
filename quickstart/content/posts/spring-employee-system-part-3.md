+++
title = 'Spring Employee System Part 3'
date = 2024-02-10T11:31:48+08:00
draft = true
+++

In Part 3, we introduce steps setting frontend Vue.js project:

[Source code](https://github.com/yennanliu/SpringPlayground/tree/main/springEmployeeSystem)

<!--more-->

Setting up the Vue Project Steps :

1. Navigate to the Frontend Directory:

```bash
cd springEmployeeSystem/frontend
```

2. Initialize the Vue Project:


```bash
vue create employee-system-ui

# Choose Vue 2 when prompted.
```

3. Install Vue Router:

```bash
vue add router
```

Vue Router is a necessary dependency for handling navigation in Vue.js applications.


4. Install Axios:

```bash
npm install --save axios
```

Axios is a promise-based HTTP client for making requests to backend APIs.

5. Install SweetAlert:

```bash
npm install --save sweetalert
```

SweetAlert is a beautiful, responsive, customizable popup box library.

6. Install Vue FullCalendar:

```bash
npm install vue-fullcalendar
```

Vue FullCalendar is a wrapper for the FullCalendar library, allowing you to easily integrate calendar functionality into your Vue.js application.

7. Install Vue2 Datepicker:

```bash
npm install vue-fullcalendar
```

bash
Copy code
npm install vue2-datepicker
Vue2 Datepicker provides a configurable date picker component for Vue.js.

8. Install other dep:

```bash
npm install bootstrap-vue
```

9. build

```bash
npm run build
```

9. Run FE app

```bash
npm run serve
```

With these steps completed, your Vue.js frontend project for the Spring Employee System should be set up and ready for development. You can further customize and expand upon it to meet your project requirements.