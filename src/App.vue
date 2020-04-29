<template>
  <div id="app">
    <header-component />
    <!-- Title Section -->
    <welcome-component />
    <!-- Title Section -->
    <bio-component />
    <div style="width:20%;">
      Nam ut lectus et risus viverra maximus. Maecenas ut lectus aliquam ligula pharetra vestibulum. Praesent gravida porta mauris, non blandit felis dignissim in. Mauris sodales iaculis enim ac eleifend. Suspendisse ultricies erat vitae porta egestas. Curabitur commodo tellus ut lobortis aliquet. Maecenas viverra arcu ut ligula venenatis, ut dictum elit condimentum. Fusce luctus enim et leo laoreet, ac ultrices diam vulputate. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Sed bibendum blandit nulla, eget congue nisi finibus vitae. Phasellus rutrum varius nisi, quis elementum dui dignissim et. Morbi ornare enim sapien, ut accumsan nibh laoreet id. Donec quis tellus eget nibh iaculis ultrices. Vivamus a neque aliquam, feugiat enim sed, vestibulum nunc. Integer vitae nunc justo. Integer erat augue, accumsan vitae massa in, mattis laoreet libero.

Quisque tellus ante, cursus ac fringilla vitae, tincidunt eget dolor. Vestibulum dignissim congue neque, non cursus mi interdum a. Vivamus ullamcorper tortor purus, sit amet aliquam risus lobortis sit amet. In eleifend erat quis aliquet feugiat. Sed scelerisque venenatis orci. Donec vitae laoreet ante. Cras consectetur est et nisi cursus gravida. Sed mollis in leo sed lacinia. Duis ultrices aliquam mattis. Praesent vel tortor eu risus dignissim laoreet at sit amet leo. Pellentesque mollis erat eget nisl tempus, id volutpat lorem condimentum. Etiam vel nisl sollicitudin ex imperdiet ornare eget ut risus. Aliquam vestibulum hendrerit aliquam. Morbi a vehicula ante. Aliquam sagittis sem vel nibh elementum lobortis a porttitor ante. Donec pellentesque sem quis turpis tristique iaculis.

Duis felis felis, dapibus nec tristique ut, consequat eu arcu. Proin fermentum ligula vel maximus rhoncus. Sed euismod augue ut bibendum viverra. Nunc tristique tincidunt urna eu bibendum. Proin et libero sed libero vestibulum convallis. Fusce aliquet libero vitae semper ultricies. Praesent lacinia luctus ante, non volutpat quam. Quisque sed hendrerit enim, id fermentum lectus. Nunc aliquet, arcu ut porta tristique, augue tellus elementum ligula, sed porta massa mi a lorem. Vivamus ultricies erat mattis magna feugiat viverra. Quisque arcu purus, scelerisque id ex id, rhoncus luctus enim. Proin vitae mi viverra, porttitor lorem sed, gravida enim. Donec viverra ante ac cursus tempus.

Vivamus molestie neque in augue dignissim fringilla nec gravida odio. Sed consectetur placerat ligula, sit amet ultricies metus congue in. Suspendisse eget nulla odio. Nullam ornare enim hendrerit euismod ultricies. Cras quis ligula et orci consectetur molestie. Vestibulum dignissim, ipsum non venenatis volutpat, augue velit lobortis augue, nec rhoncus leo metus nec ante. Nam non blandit felis, tempor luctus orci.

Mauris ultricies, nisl eu accumsan mattis, metus libero elementum leo, pretium viverra erat nulla nec odio. Cras nec purus sit amet nunc feugiat porttitor ac gravida orci. Nunc nibh augue, tristique quis mauris nec, sagittis laoreet lectus. Fusce laoreet fermentum erat. Sed eu neque porta, bibendum urna non, condimentum metus. Sed eleifend bibendum justo faucibus tincidunt. Quisque leo orci, sollicitudin eget erat malesuada, eleifend tristique ante.
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Welcome from './components/Welcome.vue'
import Bio from './components/Bio.vue'

export default {
  name: 'App',
  components: {
    'header-component': Header,
    'welcome-component': Welcome,
    'bio-component': Bio
  }
}
</script>
