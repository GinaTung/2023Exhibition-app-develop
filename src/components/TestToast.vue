<template>
    <button
        type="button"
        class="btn btn-primary"
        id="liveToastBtn"
    >
        Show live toast
    </button>

    <div
        class="position-fixed bottom-0 end-0 p-3"
        style="z-index: 11"
    >
        <div
            id="liveToast"
            class="toast"
            role="alert"
            aria-live="assertive"
            aria-atomic="true"
        >
            <div class="toast-header">
                <img
                    src="https://fakeimg.pl/30/"
                    class="rounded me-2"
                    alt="photo"
                />
                <strong class="me-auto">Bootstrap</strong>
                <small>11 mins ago</small>
                <button
                    type="button"
                    class="btn-close"
                    data-bs-dismiss="toast"
                    aria-label="Close"
                ></button>
            </div>
            <div class="toast-body">Hello, world! This is a toast message.</div>
        </div>
    </div>
</template>

<script>
    import { Toast } from 'bootstrap'
    export default {
        mounted() {
            var toastTrigger = document.getElementById('liveToastBtn')
            var toastLiveExample = document.getElementById('liveToast')
            if (toastTrigger) {
                toastTrigger.addEventListener('click', function () {
                    var toast = new Toast(toastLiveExample)

                    toast.show()
                })
            }
        }
    }
</script>

<style lang="scss" scoped></style>
