<script>
import axios from 'axios';
import data from './Data'

// let data = []
// let error = null
// onMount(async ()=>{
//     try {
//         const res = await axios.get('https://jsonplaceholder.typicode.com/users')
//         console.log(res.data)
//     } catch (e) {
//         error = e
//         console.log(error)
//     }
// })

let filters = '/assets/filter.png'

function round(number) {
    number = (Number(number) + Number.EPSILON) * 100
    return Math.round(number) / 100
}
</script>

<section class="w-[95%] overflow-x-hidden bg-black rounded-md my-[30px]">
    <div class="overflow-hidden space-y-4">
        <div class='absolute -mt-[30px] bg-black rounded-md'>
            <div class='text-white px-6 py-2 flex'>
                <img src={filters} alt="filters icon">
                <h1>All Rides</h1>
            </div>
        </div>
        <div class='px-4 py-2 overflow-hidden'>
            <div class='overflow-x-scroll mx-6 py-2 scroll-py-4 scrollbar scroll-smooth'>
                <table>
                    <tr class="p-2 bg-[#313131] text-[#00d8d8]">
                        <th class="py-2 text-center">Map</th>
                        <th class="py-2 text-center">Title</th>
                        <th class="py-2 text-center">Q Score</th>
                        <th class="py-2 text-center">From</th>
                        <th class="py-2 text-center">To</th>
                        <th class="py-2 text-center">Distance</th>
                        <th class="py-2 text-center">Q Score</th>
                        <th class="py-2 text-center">From</th>
                        <th class="py-2 text-center">To</th>
                        <th class="py-2 text-center">Distance</th>
                    </tr>
                    {#each data as ele}
                    <tr class="whitespace-nowrap text-[#a8a8a8]">
                        <td class='p-2 border-b-[1px]'>
                            <div>{ele._id}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{ele.title}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{round(ele.qScore)}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{ele.startedAt}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{ele.endedAt}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{round(ele.distance)}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{round(ele.qScore)}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{ele.startedAt}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{ele.endedAt}</div>
                        </td>
                        <td class='p-2 border-b-[1px]'>
                            <div class="border-l-[1px] px-8">{round(ele.distance)}</div>
                        </td>
                    </tr>
                    {/each}
                </table>
            </div>
        </div>
    </div>
</section>
