<script>
	import { onMount } from 'svelte';
	// this custom element is safe to import on server & client
	// it uses a newer version of lit that doesn't reference `window` at the top level of a script
	import('@aurodesignsystem/auro-button');
  import('@aurodesignsystem/auro-badge');
	import('@aurodesignsystem/auro-hyperlink');
	import('@aurodesignsystem/auro-input');
  import('@aurodesignsystem/auro-icon');
  import('@aurodesignsystem/auro-accordion');
  import('@aurodesignsystem/auro-alert');
  import('@aurodesignsystem/auro-avatar');
  // import('@aurodesignsystem/auro-background');
  import('@aurodesignsystem/auro-header');
  // import('@aurodesignsystem/auro-backtotop');
  // import('@aurodesignsystem/auro-banner');
  // import('@aurodesignsystem/auro-card');
  // import('@aurodesignsystem/auro-carousel');
  // import('@aurodesignsystem/auro-checkbox');
  import('@aurodesignsystem/auro-datetime');
  // import('@aurodesignsystem/auro-dialog');
  // import('@aurodesignsystem/auro-drawer');
  import('@aurodesignsystem/auro-flight');
  import('@aurodesignsystem/auro-loader');
  import('@aurodesignsystem/auro-lockup');
  import('@aurodesignsystem/auro-nav');
  import('@aurodesignsystem/auro-radio');
  import('@aurodesignsystem/auro-skeleton');
  import('@aurodesignsystem/auro-sidenav');
  // import('@aurodesignsystem/auro-table');
  // import('@aurodesignsystem/auro-toast');

	onMount(() => {
		// this component relies on an old version of lit that references `window` directly
		// we need to import it inside `onMount`, so that it's only imported on the client (where window is available)
		// ---------------------------------------------------------------

    // file:///Users/dalesande/src/personal/sveltekit-auro/node_modules/@aurodesignsystem/auro-dropdown/lib/popover.js:6
    // import { createPopper } from '@popperjs/core/dist/esm/popper.js';
    //         ^^^^^^^^^^^^
    // SyntaxError: Named export 'createPopper' not found. The requested module '@popperjs/core/dist/esm/popper.js' is a CommonJS module, which may not support all module.exports as named exports.
    // CommonJS modules can always be imported via the default export, for example using:
    // import pkg from '@popperjs/core/dist/esm/popper.js';
    // const { createPopper } = pkg;
    // import('@aurodesignsystem/auro-dropdown');

    // dependency on dropdown
    import('@aurodesignsystem/auro-combobox');

    // ReferenceError: window is not defined
    // /mark.js/dist/mark.min.js
    // import('@aurodesignsystem/auro-menu');

    // This will be the last one to try and make work
    import('@aurodesignsystem/auro-datepicker');

    // (node:29857) Warning: To load an ES module, set "type": "module" in the package.json or use the .mjs extension.
    // (Use `node --trace-warnings ...` to show where the warning was created)
    // /Users/dalesande/src/personal/sveltekit-auro/node_modules/dayjs/esm/index.js:1
    // import * as C from './constant';
    // import('@aurodesignsystem/auro-pane');

    // import('@aurodesignsystem/auro-popover');

    // import('@aurodesignsystem/auro-select');
	});
</script>

<!-- <style>
  auro-* {
    display: block;
    padding: 0 20px;
  }
</style> -->

<auro-accordion>
  <span slot="trigger">Trigger</span>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </p>
  <p>
    Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
  </p>
  <p>
    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
  </p>
  <p>
    Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>
</auro-accordion>

<div style="display: flex;">

  <div style="width: 50%;">
    <auro-badge>hello world</auro-badge>

    <auro-radio-group>
      <span slot="legend">Form label goes here</span>
      <auro-radio id="radio28" label="Yes" name="radioDemo" value="yes"></auro-radio>
      <auro-radio id="radio29" label="No" name="radioDemo" value="no"></auro-radio>
      <auro-radio id="radio30" label="Maybe" name="radioDemo" value="maybe"></auro-radio>
    </auro-radio-group>

    <!-- <auro-background bg="url(https://sitecore-test-single-westus2.azurewebsites.net/-/media/Images/pages/examples/ad2) center center/cover no-repeat">
      <div style="color: var(--ds-color-text-primary-inverse); display: flex; flex-direction: column; align-items: center; justify-content: center;">
        <auro-header level="2" display="600">View all destinations</auro-header>
        <auro-hyperlink cta href="#">See where we fly</auro-hyperlink>
      </div>
    </auro-background> -->

    <!-- <auro-carousel label="Images" scrolldistance="600">
      <img src="https://picsum.photos/200?random=0" alt="Random insert 0">
      <img src="https://picsum.photos/200?random=1" alt="Random insert 1">
      <img src="https://picsum.photos/200?random=2" alt="Random insert 2">
      <img src="https://picsum.photos/200?random=3" alt="Random insert 3">
      <img src="https://picsum.photos/200?random=4" alt="Random insert 4">
      <img src="https://picsum.photos/200?random=5" alt="Random insert 5">
      <img src="https://picsum.photos/200?random=6" alt="Random insert 6">
      <img src="https://picsum.photos/200?random=7" alt="Random insert 7">
      <img src="https://picsum.photos/200?random=8" alt="Random insert 8">
      <img src="https://picsum.photos/200?random=9" alt="Random insert 9">
      <img src="https://picsum.photos/200?random=10" alt="Random insert 10">
      <img src="https://picsum.photos/200?random=11" alt="Random insert 11">
      <img src="https://picsum.photos/200?random=12" alt="Random insert 12">
      <img src="https://picsum.photos/200?random=13" alt="Random insert 13">
      <img src="https://picsum.photos/200?random=14" alt="Random insert 14">
      <img src="https://picsum.photos/200?random=15" alt="Random insert 15">
      <img src="https://picsum.photos/200?random=16" alt="Random insert 16">
      <img src="https://picsum.photos/200?random=17" alt="Random insert 17">
      <img src="https://picsum.photos/200?random=18" alt="Random insert 18">
      <img src="https://picsum.photos/200?random=19" alt="Random insert 19">
      <img src="https://picsum.photos/200?random=20" alt="Random insert 20">
      <img src="https://picsum.photos/200?random=21" alt="Random insert 21">
      <img src="https://picsum.photos/200?random=22" alt="Random insert 22">
      <img src="https://picsum.photos/200?random=23" alt="Random insert 23">
      <img src="https://picsum.photos/200?random=24" alt="Random insert 24">
      <img src="https://picsum.photos/200?random=25" alt="Random insert 25">
      <img src="https://picsum.photos/200?random=26" alt="Random insert 26">
      <img src="https://picsum.photos/200?random=27" alt="Random insert 27">
      <img src="https://picsum.photos/200?random=28" alt="Random insert 28">
      <img src="https://picsum.photos/200?random=29" alt="Random insert 29">
      <img src="https://picsum.photos/200?random=30" alt="Random insert 30">
      <img src="https://picsum.photos/200?random=31" alt="Random insert 31">
      <img src="https://picsum.photos/200?random=32" alt="Random insert 32">
      <img src="https://picsum.photos/200?random=33" alt="Random insert 33">
      <img src="https://picsum.photos/200?random=34" alt="Random insert 34">
      <img src="https://picsum.photos/200?random=35" alt="Random insert 35">
      <img src="https://picsum.photos/200?random=36" alt="Random insert 36">
      <img src="https://picsum.photos/200?random=37" alt="Random insert 37">
      <img src="https://picsum.photos/200?random=38" alt="Random insert 38">
      <img src="https://picsum.photos/200?random=39" alt="Random insert 39">
      <img src="https://picsum.photos/200?random=40" alt="Random insert 40">
      <img src="https://picsum.photos/200?random=41" alt="Random insert 41">
      <img src="https://picsum.photos/200?random=42" alt="Random insert 42">
      <img src="https://picsum.photos/200?random=43" alt="Random insert 43">
      <img src="https://picsum.photos/200?random=44" alt="Random insert 44">
      <img src="https://picsum.photos/200?random=45" alt="Random insert 45">
      <img src="https://picsum.photos/200?random=46" alt="Random insert 46">
      <img src="https://picsum.photos/200?random=47" alt="Random insert 47">
      <img src="https://picsum.photos/200?random=48" alt="Random insert 48">
      <img src="https://picsum.photos/200?random=49" alt="Random insert 49">
      <img src="https://picsum.photos/200?random=50" alt="Random insert 50">
      <img src="https://picsum.photos/200?random=51" alt="Random insert 51">
      <img src="https://picsum.photos/200?random=52" alt="Random insert 52">
      <img src="https://picsum.photos/200?random=53" alt="Random insert 53">
      <img src="https://picsum.photos/200?random=54" alt="Random insert 54">
      <img src="https://picsum.photos/200?random=55" alt="Random insert 55">
      <img src="https://picsum.photos/200?random=56" alt="Random insert 56">
      <img src="https://picsum.photos/200?random=57" alt="Random insert 57">
      <img src="https://picsum.photos/200?random=58" alt="Random insert 58">
      <img src="https://picsum.photos/200?random=59" alt="Random insert 59">
      <img src="https://picsum.photos/200?random=60" alt="Random insert 60">
      <img src="https://picsum.photos/200?random=61" alt="Random insert 61">
      <img src="https://picsum.photos/200?random=62" alt="Random insert 62">
      <img src="https://picsum.photos/200?random=63" alt="Random insert 63">
      <img src="https://picsum.photos/200?random=64" alt="Random insert 64">
      <img src="https://picsum.photos/200?random=65" alt="Random insert 65">
      <img src="https://picsum.photos/200?random=66" alt="Random insert 66">
      <img src="https://picsum.photos/200?random=67" alt="Random insert 67">
      <img src="https://picsum.photos/200?random=68" alt="Random insert 68">
      <img src="https://picsum.photos/200?random=69" alt="Random insert 69">
      <img src="https://picsum.photos/200?random=70" alt="Random insert 70">
      <img src="https://picsum.photos/200?random=71" alt="Random insert 71">
      <img src="https://picsum.photos/200?random=72" alt="Random insert 72">
      <img src="https://picsum.photos/200?random=73" alt="Random insert 73">
      <img src="https://picsum.photos/200?random=74" alt="Random insert 74">
      <img src="https://picsum.photos/200?random=75" alt="Random insert 75">
      <img src="https://picsum.photos/200?random=76" alt="Random insert 76">
      <img src="https://picsum.photos/200?random=77" alt="Random insert 77">
      <img src="https://picsum.photos/200?random=78" alt="Random insert 78">
      <img src="https://picsum.photos/200?random=79" alt="Random insert 79">
      <img src="https://picsum.photos/200?random=80" alt="Random insert 80">
      <img src="https://picsum.photos/200?random=81" alt="Random insert 81">
      <img src="https://picsum.photos/200?random=82" alt="Random insert 82">
      <img src="https://picsum.photos/200?random=83" alt="Random insert 83">
      <img src="https://picsum.photos/200?random=84" alt="Random insert 84">
      <img src="https://picsum.photos/200?random=85" alt="Random insert 85">
      <img src="https://picsum.photos/200?random=86" alt="Random insert 86">
      <img src="https://picsum.photos/200?random=87" alt="Random insert 87">
      <img src="https://picsum.photos/200?random=88" alt="Random insert 88">
      <img src="https://picsum.photos/200?random=89" alt="Random insert 89">
      <img src="https://picsum.photos/200?random=90" alt="Random insert 90">
      <img src="https://picsum.photos/200?random=91" alt="Random insert 91">
      <img src="https://picsum.photos/200?random=92" alt="Random insert 92">
      <img src="https://picsum.photos/200?random=93" alt="Random insert 93">
      <img src="https://picsum.photos/200?random=94" alt="Random insert 94">
      <img src="https://picsum.photos/200?random=95" alt="Random insert 95">
      <img src="https://picsum.photos/200?random=96" alt="Random insert 96">
      <img src="https://picsum.photos/200?random=97" alt="Random insert 97">
      <img src="https://picsum.photos/200?random=98" alt="Random insert 98">
      <img src="https://picsum.photos/200?random=99" alt="Random insert 99">
    </auro-carousel> -->

    <auro-pane date="2020-09-20"></auro-pane>
    <auro-pane date="2020-09-21" selected></auro-pane>
    <auro-pane date="2020-09-22" disabled></auro-pane>

    <!-- <auro-checkbox-group>
      <span slot="legend">Form label goes here</span>
      <auro-checkbox value="checkbox option" name="example1" id="checkbox-basic1">Checkbox option</auro-checkbox>
      <auro-checkbox value="checkbox option" name="example2" id="checkbox-basic2" checked>Checkbox option</auro-checkbox>
      <auro-checkbox value="checkbox option" name="example3" id="checkbox-basic3">Checkbox option</auro-checkbox>
      <auro-checkbox value="checkbox option" name="example4" id="checkbox-basic4">Checkbox option</auro-checkbox>
    </auro-checkbox-group> -->

    <!-- <auro-toast style="display: block; margin: 0.5rem 0;"id="defaultToast">
      Default notification with no error type
    </auro-toast> -->

    <auro-datepicker>
      <span slot="fromLabel">Choose a date</span>
      <span slot="mobileDateLabel">Choose a date</span>
    </auro-datepicker>

    <auro-datetime type="date"></auro-datetime>

    <auro-hyperlink
      target="_blank"
      href="https://www.alaskaair.com">
      external target
    </auro-hyperlink>

    <auro-alert type="information">You are confirmed on Flight 20 to Aruba.</auro-alert>

    <auro-avatar code="boi"></auro-avatar>
    <auro-avatar type="md" code="anc"></auro-avatar>
    <auro-avatar type="sm" code="mke"></auro-avatar>

    <auro-header>Hello World!</auro-header>

    <auro-input bordered></auro-input>

    <auro-icon category="interface" name="pin-trip"></auro-icon>

    <auro-combobox>
      <span slot="label">Name</span>
      <auro-menu>
        <auro-menuoption value="Apples" id="option-0">Apples</auro-menuoption>
        <auro-menuoption value="Oranges" id="option-1">Oranges</auro-menuoption>
        <auro-menuoption value="Peaches" id="option-2">Peaches</auro-menuoption>
        <auro-menuoption value="Grapes" id="option-3">Grapes</auro-menuoption>
        <auro-menuoption value="Cherries" id="option-4">Cherries</auro-menuoption>
        <auro-menuoption static nomatch>No matching option</auro-menuoption>
      </auro-menu>
    </auro-combobox>

    <auro-sidenav>
      <span slot="heading">Pet travel policies</span>
      <auro-sidenavitem href="/content/travel-info/pets">Pet travel overview</auro-sidenavitem>
      <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-with-pets/pets-in-cabin">Pets in cabin</auro-sidenavitem>
      <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-with-pets/pets-in-baggage-compartment">Pets in baggage compartment</auro-sidenavitem>
      <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-hawaii">Traveling to Hawaii</auro-sidenavitem>
      <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-international" target="_blank">International travel with pets</auro-sidenavitem>
      <auro-sidenavsection>
        <span slot="trigger">FAQ</span>
        <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-with-pets/banfield-qa#safe-to-fly">Is it safe to fly with my pet?</auro-sidenavitem>
        <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-with-pets/banfield-qa#certain-breeds-prohibited">Why are certain breeds prohibited from flying in the cargo compartment?</auro-sidenavitem>
        <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-with-pets/banfield-qa#dog-info" target="_blank">Dogs</auro-sidenavitem>
        <auro-sidenavitem href="/content/travel-info/policies/pets-traveling-with-pets/banfield-qa#cat-info" target="_blank">Cats</auro-sidenavitem>
      </auro-sidenavsection>
    </auro-sidenav>

    <!-- Svelte does not like data in the HTML. But the imported element data works.  -->
    <!-- <auro-table
      nowrap
      columnHeaders='["","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday","Sunday"]'
      componentData='[
        {"": "Dance class", "Monday": "5:00pm","Wednesday": "5:00pm" },
        {"": "Night classes", "Thursday": "7:00pm","Friday": "7:00pm" },
        {"": "Team meeting", "Wednesday": "10:00am" },
        {"": "Morning workout", "Monday": "8:00am", "Tuesday": "8:00am", "Wednesday": "8:00am", "Thursday": "8:00am", "Friday": "8:00am" }
      ]'>
    </auro-table> -->
  </div>

  <div>

    <auro-skeleton shape="circle" style="width: 40px; height: 40px"></auro-skeleton>
    <auro-skeleton shape="oval" style="width: 200px; height: 100px;"></auro-skeleton>
    <auro-skeleton shape="rectangle" style="width: 400px; height: 300px"></auro-skeleton>

    <auro-flight
      flights='["AS 374"]'
      duration="120"
      departureTime="2022-05-04T01:55:00-09:00"
      departureStation="ANC"
      arrivalTime="2022-05-04T03:55:00-09:00"
      arrivalStation="ADK">
      <auro-flightline>
        <auro-flight-segment stopover iata="CDB"></auro-flight-segment>
      </auro-flightline>
    </auro-flight>

    <auro-button>hello world</auro-button>

    <auro-lockup>
      <span slot="title">Place title text here</span>
      <span slot="subtitle">Place subtitle text here</span>
    </auro-lockup>

    <auro-nav>
      <auro-breadcrumb href="http://auro.alaskaair.com/components/auro/nav">Home</auro-breadcrumb>
      <auro-breadcrumb href="http://auro.alaskaair.com/components/auro/nav">Level 2</auro-breadcrumb>
      <auro-breadcrumb href="http://auro.alaskaair.com/components/auro/nav">Level 3</auro-breadcrumb>
      <auro-breadcrumb href="http://auro.alaskaair.com/components/auro/nav">Level 4</auro-breadcrumb>
      <auro-breadcrumb>Current</auro-breadcrumb>
    </auro-nav>

    <!-- <auro-banner billboard>
      <picture slot="displayImage">
        <source srcset="https://picsum.photos/id/430/1124/800" media="(min-width: 1024px)">
        <source srcset="https://picsum.photos/id/430/1124/1000" media="(min-width: 768px)">
        <source srcset="https://picsum.photos/id/430/736/750" media="(min-width: 736px)">
        <source srcset="https://picsum.photos/id/430/736/1400" media="(min-width: 375px)">
        <source srcset="https://picsum.photos/id/430/320/700" media="(min-width: 320px)">
        <img src="https://picsum.photos/id/430/225/550" alt="" />
      </picture>
      <img
        slot="contentImage"
        src="https://sitecore-test-single-westus2.azurewebsites.net/-/media/Images/pages/examples/oneworld-travel-bright-Horizontal-300.png"
        alt="Random insert"/>
      <p slot="description">
        We’ll explain any additional costs before you book your car rental. More details on what’s included? Just check the Ts&Cs of any car.
      </p>

      <auro-hyperlink
        cta
        secondary
        href="/"
        slot="action"
        target="_blank">
        More info
      </auro-hyperlink>
    </auro-banner> -->

    <auro-loader ringworm></auro-loader>
    <auro-loader orbit></auro-loader>
    <auro-loader pulse></auro-loader>
    <auro-loader laser></auro-loader>

    <!-- <auro-backtotop>Back to top</auro-backtotop> -->

    <!-- <auro-card>
      <span slot="title">
        Pri dicat graece abhorreant
      </span>
      <img
        slot="image"
        src="https://picsum.photos/304?random=0"
        alt="Random insert 0"/>
      <p slot="description">
        Ei est detracto fabellas convenire, vivendo accusata intellegebat ex mei. Pri dicat graece abhorreant ut, sea ei vidit omnes, errem tempor eligendi cu eos.
      </p>
      <auro-hyperlink
        nav
        href="/"
        slot="action"
        target="_blank">
        More info
      </auro-hyperlink>
      <p slot="disclaimer">
        * Errem tempor eligendi cu eos
      </p>
    </auro-card> -->

    <p id="foo">The element is labelled by content external to the element.</p>
    <auro-dropdown id="commonAdvanced" aria-labelledby="foo" bordered rounded inset chevron>
      <div style="padding: var(--ds-size-150);">
        Lorem ipsum solar
        <br />
        <auro-button onclick="document.querySelector('#commonAdvanced').hide()">
          Dismiss Dropdown
        </auro-button>
      </div>
      <span slot="helpText">
        Help text
      </span>
      <div slot="trigger">
        Trigger
      </div>
    </auro-dropdown>
  </div>
</div>

<!-- <auro-dialog id="defaultDialog">
  <span slot="header">Default Dialog</span>
  <div slot="content">
    <p>When traveling on Alaska Airlines flights, Alaska Airlines checked baggage fees may apply. See <auro-hyperlink href="https://www.alaskaair.com/bagrules" target="_blank">alaskaair.com/bagrules</auro-hyperlink> for our rules. For itineraries that include other airlines, their checked baggage fees may apply, as displayed on their websites.</p>
    <p>Baggage rules and fees will be based on the specific itinerary chosen. The applicable first and second bag fees will be displayed after you have added flights to the cart.</p>
    <auro-header level="3" display="500">Before checking your bags, remember to:</auro-header>
    <ul>
      <li>Caerphilly croque monsieur fondue</li>
      <li>Taleggio goat mascarpone cow manchego cheese and wine emmental cheese strings</li>
      <li>Cheddar cheese and biscuits chalk and cheese</li>
      <li>Camembert de normandie stinking bishop bavarian bergkase</li>
    </ul>
  </div>
  <div slot="footer" class="auro_containedButtons">
    <auro-button secondary onClick="toggleInterruption('#defaultDialog')">Close</auro-button>
  </div>
</auro-dialog> -->

<!-- <auro-drawer id="defaultDrawer">
  <span slot="header">Default Drawer</span>
  <div slot="content">
    <p>When traveling on Alaska Airlines flights, Alaska Airlines checked baggage fees may apply. See <auro-hyperlink href="https://www.alaskaair.com/bagrules" target="_blank">alaskaair.com/bagrules</auro-hyperlink> for our rules. For itineraries that include other airlines, their checked baggage fees may apply, as displayed on their websites.</p>
    <p>Baggage rules and fees will be based on the specific itinerary chosen. The applicable first and second bag fees will be displayed after you have added flights to the cart.</p>
    <auro-header level="3" display="500">Before checking your bags, remember to:</auro-header>
    <ul>
      <li>Caerphilly croque monsieur fondue</li>
      <li>Taleggio goat mascarpone cow manchego cheese and wine emmental cheese strings</li>
      <li>Cheddar cheese and biscuits chalk and cheese</li>
      <li>Camembert de normandie stinking bishop bavarian bergkase</li>
    </ul>
  </div>
  <div slot="footer" class="auro_containedButtons">
    <auro-button secondary onClick="toggleInterruption('#defaultDialog')">Close</auro-button>
  </div>
</auro-drawer> -->
