<template>
  <div class="page">
    <h1 id="api-reference" class="mb-3">
      <router-link to="/api-reference#api-reference" class="header-anchor">
        <span class="header-anchor--hash">#</span>
        API Reference
      </router-link>
    </h1>

    <h2 id="api-reference-component" class="mb-4 text-muted">
      <router-link
        to="/api-reference#api-reference-component"
        class="header-anchor"
      >
        <span class="header-anchor--hash">#</span>
        <code>&lt;runtime-template-compiler&gt;</code>
      </router-link>
    </h2>

    <p>
      <code>&lt;runtime-template-compiler&gt;</code> is the component for
      enabling the compilation of templates at runtime. It takes the data
      computed method and other required properties from the parent component
      and merges them into a new one which is then merged with the results of
      the <code>vue-template-compiler</code> liraray, it is then rendered using
      the
      <a
        href="https://vuejs.org/"
        target="_blank"
        rel="nofollow"
        class="external"
        >Vue.js<i class="fas fa-external-link-alt"></i
      ></a>
      <code class="ml-1">&lt;component&gt;</code> component. This allows all of
      the normal
      <a
        href="https://vuejs.org/"
        target="_blank"
        rel="nofollow"
        class="external"
        >Vue.js<i class="fas fa-external-link-alt"></i
      ></a>
      bindings to work on the compiled template.
    </p>

    <h2 id="api-reference-props" class="mb-4 text-mmuted">
      <router-link
        to="/api-reference#api-reference-props"
        class="header-anchor"
      >
        <span class="header-anchor--hash">#</span>
        Props
      </router-link>
    </h2>

    <h3 id="api-reference-props-template" class="mb-4 text-muted">
      <router-link
        to="/api-reference#api-reference-props-template"
        class="header-anchor"
      >
        <span class="header-anchor--hash">#</span>
        template
      </router-link>
    </h3>

    <ul>
      <li>Type: <code>String</code></li>
      <li>Required</li>
      <li>
        The HTML template string that we would like to compile and bind data
        too.
        <pre
          class="language-js mb-4"
        ><code>{{ templatePropExample | trim }}</code></pre>
      </li>
    </ul>

    <h3 id="api-reference-props-parent" class="mb-4 text-muted">
      <router-link
        to="/api-reference#api-reference-props-parent"
        class="header-anchor"
      >
        <span class="header-anchor--hash">#</span>
        parent
      </router-link>
    </h3>

    <ul>
      <li>Type: <code>Object&lt;Component&gt;</code></li>
      <li>Optional</li>
      <li>
        The parent component we would like to fetch and bind data from.
        <pre
          class="language-js mb-4"
        ><code>{{ parentPropExample | trim }}</code></pre>
      </li>
    </ul>

    <h3 id="api-reference-props-compiler-options" class="mb-4 text-muted">
      <router-link
        to="/api-reference#api-reference-props-compiler-options"
        class="header-anchor"
      >
        <span class="header-anchor--hash">#</span>
        compilerOptions
      </router-link>
    </h3>

    <ul>
      <li>Type: <code>Object</code></li>
      <li>Optional</li>
      <li>
        The options to pass along to the <code>vue-template-compiler</code>.
        Check out the
        <a
          href="https://github.com/vuejs/vue/tree/dev/packages/vue-template-compiler#readme"
          target="_blank"
          rel="nofollow"
          class="external"
          >documentation<i class="fas fa-external-link-alt"
        /></a>
        for all of the avaliable options.
        <pre
          class="language-js mb-4"
        ><code>{{ compileOptionsExample | trim }}</code></pre>
      </li>
    </ul>

    <PageNav>
      <template v-slot:left>
        <router-link to="/guide/filters">
          <i class="fas fa-arrow-left"></i>
          Filters
        </router-link>
      </template>
      <template v-slot:right>
        <router-link to="/sandbox">
          Sandbox
          <i class="fas fa-arrow-right"></i>
        </router-link>
      </template>
    </PageNav>
  </div>
</template>

<script>
import PageNav from '../components/PageNav.vue'

export default {
  name: 'ApiReference',

  components: {
    PageNav
  },

  data() {
    return {
      templatePropExample: '<runtime-template-compiler :template="template" />',
      parentPropExample: '<runtime-template-compiler :parent="parent" />',
      compileOptionsExample:
        '<runtime-template-compiler :compiler-options="options" />'
    }
  }
}
</script>
