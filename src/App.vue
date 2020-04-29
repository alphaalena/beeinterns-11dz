<template>
  <div id="app">
    <header-component>
      <logo class="margin-right-big"/>
      <input-component class="width-input" right-input placeholder="Search for Products"/>
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
      <column-component>
        <heading-component class="heading-main">Seller Application</heading-component>
        <row-component>
          <button-component type="flat" :key="button" v-for="button in buttons">{{button}}</button-component>
        </row-component>
        <row-component>
          <registration-component>
            <row-component>
              <input-component class="marginForm" :key="name.placeholder" v-for="name in names"
                               :placeholder='name.placeholder' :label="name.label"/>
            </row-component>
            <row-component>
              <input-component class="width100 marginForm" :key="title.placeholder" v-for="title in titles"
                               :placeholder='title.placeholder' :label="title.label"/>
            </row-component>
            <separator-component>
              <div class="signature ">Business Mailing Address</div>
            </separator-component>
            <row-component>
              <input-component :key="address.label" v-for="address in addresses" :label="address.label"/>
            </row-component>
            <row-component>
              <template v-for="(index, i) in indexes">
                <input-component :key="index.label" :placeholder="index.placeholder"
                                 :label="index.label" :text="index.text" class="flex-1"/>
                <spacer-component :key="index.label + 'spacer'" v-if="indexes.length !== i + 1"/>
              </template>
            </row-component>
            <row-component>
              <button-component type="outline">Go Back</button-component>
              <button-component type="flat">By Submitting this application,you agree to the</button-component>
              <button-component class="margin-top" type="filled">Submit Application</button-component>
            </row-component>
          </registration-component>
        </row-component>
      </column-component>
    </main-component>
    <footer-component >
      <row-component align-items>
        <column-component :key="column.title" v-for="column in columns">
          <heading-component class="flex-1 margin-right heading-footer">{{column.title}}</heading-component>
          <wrapper-links-component  class="flex-1 margin-right" v-for="link in column.links" :key="link.title">
           <icon-component :icon-name="link.icon" v-if="link.icon"/>
           <link-component link-black>{{link.title}}</link-component>
          </wrapper-links-component>
        </column-component>
      </row-component>
      <separator-component class="marginForm margin-bottom"/>
      <row-component>
        <button-component type="flat" class="margin-bottom" margin-center>Terms & Conditions Privacy</button-component>
      </row-component>
    </footer-component>
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
import RowComponent from './components/row-component'
import RegistrationComponent from './components/registration-component'
import SeparatorComponent from './components/separator-component'
import FooterComponent from './components/footer-component'
import ColumnComponent from './components/column-component'
import SpacerComponent from './components/spacer-component'
import WrapperLinksComponent from './components/wrapperLinks.component'

export default {
  name: 'App',
  components: {
    WrapperLinksComponent,
    SpacerComponent,
    ColumnComponent,
    FooterComponent,
    SeparatorComponent,
    RegistrationComponent,
    RowComponent,
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
      ],
      addresses: [
        {
          label: 'Street Address'
        },
        {
          label: 'Apt / Suite / Other'
        },
        {
          label: 'City'
        }
      ],
      indexes: [
        {
          label: 'Zip / Postal Code'
        },
        {
          placeholder: 'Select Country',
          label: 'Country'
        },
        {
          label: 'Phone Number',
          text: 'To Validate your account please enter valid mobile Number to receive confirmation code'
        }
      ],
      headings: ['How We Help', 'Get to Know Us', 'Join the Community', 'Follow Us'],
      items: ['About', 'Policies', ' Careers', ' Press'],
      columns: [
        {
          title: 'How We Help',
          links: [
            {
              title: 'Retailers'
            },
            {
              title: 'Interiors Designers'
            },
            {
              title: 'Product Designers'
            },
            {
              title: 'Wholesalers / Importers'
            },
            {
              title: 'Artisans'
            }
          ]
        },
        {
          title: 'Get to Know Us',
          links: [
            {
              title: 'About'
            },
            {
              title: 'Policies'
            },
            {
              title: 'Careers'
            },
            {
              title: 'Press'
            }
          ]
        },
        {
          title: 'Join the Community',
          links: [
            {
              title: 'Upcoming Events'
            },
            {
              title: 'Become a Buyer'
            },
            {
              title: 'Become a Seller'
            }
          ]
        },
        {
          title: 'Follow Us',
          links: [
            {
              title: 'Facebook',
              icon: 'fb icon'
            },
            {
              title: 'Pinterest',
              icon: 'pntr icon'
            },
            {
              title: 'Twitter',
              icon: 'twt icon'
            },
            {
              title: 'Instagram',
              icon: 'insta icon'
            }
          ]
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
