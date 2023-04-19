<script context="module">
    export async function load() {
      return {
        props: {
          name: 'SvelteKit'
        }
      };
    }
  </script>
  
  <script>
    export let name='';
  </script>
  
  <h1>Hello, {name}!</h1>
  