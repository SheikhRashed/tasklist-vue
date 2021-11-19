<template lang="">
    <!-- Header start  -->
    <div class="py-4 bg-green-500 hidden">
        <div class="container">
            <!-- title -->
            <h6 class="text-xl md:text-3xl text-center text-white font-semibold font-mono">
                {{ title }}
            </h6>
        </div>
    </div>
    <!-- Header end  -->
    <!-- Goals-list start -->
    <div class="relative h-screen w-full md:w-1/2 mx-auto mt-40">
        <div class="container mx-4">
            <!-- card start  -->
            <div class="relative bg-white shadow-md rounded-lg overflow-hidden">
                <!-- header start  -->
                <div class="bg-green-500 py-4">
                    <h2 class="text-center text-2xl capitalize text-white font-bold">
                        {{ cardTitle }}
                    </h2>
                </div>
                <!-- header end  -->
                <!-- Body start  -->
                <div class="p-4">
                    <!-- Add Goals Field start  -->
                    <div class="text-center relative overflow-hidden">
                        <input type="text" placeholder="add you Goals..." class="border border-gray-500 rounded-none px-4 py-2 placeholder-gray capitalize w-full" v-model="inputValue"  />
                        <button class="px-4 sm:w-36 h-full right-0 text-md d-inline absolute capitalize bg-red-600 hover:bg-red-700  text-white font-semibold" @click="addGoal" >
                            add
                        </button>
                    </div>
                    <!-- Add Goals Field end  -->

                    <!-- Goals-content start  -->
					<ul class="mt-6 p-4 bg-green-100 ">
						<!-- if there no goals Listed -->
						<li v-if="goals.length === 0"  class="flex justify-center items-center bg-white p-4 group transition-all duration-1000  ease-in-out cursor-pointer text-center " >
							<p class="text-lg tracking-wide uppercase font-bold text-red-600  group-hover:text-red-700">There are no Goals</p>
						</li>
						<!-- goal -->
						<li v-else class="flex justify-between items-center bg-green-200 hover:bg-green-400  p-4 group transition-all duration-1000  ease-in-out cursor-pointer ">
							<p class="text-lg capitalize font-semibold text-gray-600 group-hover:text-gray-900 " >Hello I'm Something to do</p>
							<!-- actions  -->
							<div class="flex flex-col sm:flex-row  items-center  space-y-2 sm:space-y-0  sm:space-x-4" >
								<!-- delete  -->
								<a href="#" class="text-gray-900 group-hover:text-red-500 " >
									<i class="fas fa-trash-alt"></i>
								</a>
								<a href="#" class="text-gray-900 " >
									<i class="far fa-edit"></i>
								</a>
							</div>
						</li>
						<!-- goal end  -->
					</ul>
                    <!-- Goals-content end  -->
                </div>
                <!-- Body end  -->
            </div>
            <!-- card end  -->
        </div>
    </div>
    <!-- Goals-list end -->
</template>
<script>
    export default {
        name: "App",
        data() {
            return {

				title: 'task List',
				placeText: "Add you goals",
				cardTitle: "List of Your Goals",
				inputValue: '',
				goals:[],
            };
        },
		methods: {

			addGoal() { 
				this.goals.push(this.inputValue) // add input in goals array
				this.inputValue = ''; // clear input after add 
			}
		},
    };
</script>
<style lang=""></style>
