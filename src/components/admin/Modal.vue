<template lang="pug">
    div
        div(:class="{'modal-frame':true, 'state-appear':status}")
            .modal
                .modal-inset
                    i.material-icons.button.close(@click="$emit('close')") close
                    .modal-body
                        slot(name="body")    
        div(:class="{'modal-overlay':true, 'state-show':status}")
            
</template>

<script>
	export default {
        props:["status"],
        name: 'Modal'
	}
</script>

<style lang="stylus">
	@import '../../styl/Modal.styl'
</style>
