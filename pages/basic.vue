<template>
    <Nav />
    <div class=" flex items-center min-h-screen">
    <div
                    class="flex flex-col max-w-lg p-6 mx-auto text-center text-gray-900 bg-white border border-gray-100 rounded-lg shadow  xl:p-8">
                    <h3 class="mb-4 text-2xl font-semibold">Standard</h3>
                    <p class="font-light text-gray-500 sm:text-lg ">Cea mai bună opțiune pentru uz personal &amp; forum
                        următorul tău proiect.</p>
                    <div class="flex items-baseline justify-center my-8">
                        <span class="mr-2 text-5xl font-extrabold">149 RON</span>
                    </div>

                    <ul role="list" class="mb-8 space-y-4 text-left">
                        <li class="flex items-center space-x-3">

                            <svg class="flex-shrink-0 w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd"
                                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                                    clip-rule="evenodd"></path>
                            </svg>
                            <span>1 oră despre comportamentul și nevoile</span>
                        </li>
                        <li class="flex items-center space-x-3">

                            <svg class="flex-shrink-0 w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd"
                                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                                    clip-rule="evenodd"></path>
                            </svg>
                            <span>Materiale educaționale digitale</span>
                        </li>
                        <li class="flex items-center space-x-3">

                            <svg class="flex-shrink-0 w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd"
                                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                                    clip-rule="evenodd"></path>
                            </svg>
                            <span>Consultație personalizată de 30 min</span>
                        </li>
                        <li class="flex items-center space-x-3">

                            <svg class="flex-shrink-0 w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20"
                                xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd"
                                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                                    clip-rule="evenodd"></path>
                            </svg>
                            <span>Acces exclusiv la un forum online</span>
                        </li>
                    </ul>
                    <div class="buttons justify-center">
                        <div id="paypal-button-container"></div>
                    </div>
                </div>
                </div>
                <Footer />
</template>


<script>
export default {
    mounted() {
        const script = document.createElement('script');
        script.src = 'https://www.sandbox.paypal.com/sdk/js?client-id=AbdSXN0YpY67db5vOguCrGUpUCcZhdU2GpAHJSfESYt0BATO1pXGh3ZV3sKWMA3EyRskMAWv6Tr7OSHC&components=buttons';
        script.addEventListener('load', this.initializePayPalButtons);
        document.body.appendChild(script);
    },
    methods: {
        initializePayPalButtons() {
            // Render PayPal buttons after SDK script is loaded
            paypal.Buttons({
                style: {
                    disableMaxWidth: true
                },
                // Define the function to be called when the user approves the payment
                onApprove: (data, actions) => {
                    // Perform the necessary actions after payment approval (e.g., save the transaction details)
                    
                    // Redirect the user to the home page
                    window.location.href = '/'; // Replace '/' with the URL of your home page
                }
            }).render('#paypal-button-container');
        }
    }
}

</script>