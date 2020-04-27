<template>
  <div id="app">
    <header-component>
      <logo class="margin-right-big"/>
      <input-component class="width-input"  right-input placeholder="Search for Products"/>
      <button-component class="margin-right-big" left-flat type="filled">Search</button-component>
      <button-component class="margin-right-little" type="outline">Log in</button-component>
      <button-component class="margin-right-little" type="outline">Sign up</button-component>
      <icon-component class="margin-right-little" icon-name="shortlist icon"/>
      <icon-component icon-name="Cart icon"/>
    </header-component>
    <navigation-component>
      <link-component :key="link" v-for="link in links">{{link}}</link-component>
    </navigation-component>
    <main-component>
      <form-component>
        <heading-component>Seller Application</heading-component>
        <row-component>
           <button-component type="flat" :key="button" v-for="button in buttons">{{button}}</button-component>
        </row-component>
        <row-component>
          <registration-component>
            <row-component>
              <input-component :key="name.placeholder" v-for="name in names" :placeholder='name.placeholder' :label="name.label"/>
            </row-component>
            <row-component>
              <input-component class="width100" :key="title.placeholder" v-for="title in titles" :placeholder='title.placeholder' :label="title.label"/>
            </row-component>
          </registration-component>
        </row-component>
      </form-component>
    </main-component>

  </div>
</template>

<script>
import headerComponent from './components/header-component.vue'
import Logo from './components/logo'
import InputComponent from './components/input-component'
import ButtonComponent from './components/button-component'
import IconComponent from './components/icon-component'
import NavigationComponent from './components/navigation-component'
import LinkComponent from './components/link-component'
import MainComponent from './components/main-component'
import HeadingComponent from './components/heading-component'
import FormComponent from './components/form-component'
import RowComponent from './components/row-component'
import RegistrationComponent from './components/registration-component'

export default {
  name: 'App',
  components: {
    RegistrationComponent,
    RowComponent,
    FormComponent,
    HeadingComponent,
    MainComponent,
    LinkComponent,
    NavigationComponent,
    IconComponent,
    ButtonComponent,
    InputComponent,
    Logo,
    headerComponent
  },
  data () {
    return {
      links: ['Home Decor', 'Furniture', 'Lighting', 'Home Accents', 'Rugs', 'Outdoors', 'Holidays', 'Gifts', 'Events'],
      buttons: ['Application Critaria', 'Company Profile', 'Web & Social Media', 'Contact Info', 'Confirm Account'],
      names: [
        {
          placeholder: 'Mr.',
          label: 'Name'
        },
        {
          placeholder: 'First Name'
        },
        {
          placeholder: 'Middle Name'
        },
        {
          placeholder: 'Last Name'
        }
      ],
      titles: [
        {
          placeholder: 'eg. CEO, Owner, Manager, Designer, Merchandiser',
          label: 'Title'
        }
      ]
    }
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Roboto, sans-serif;
  }
</style>
