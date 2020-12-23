<!-- App.svelte -->
<script>
    import './TailwindStyles.svelte';
    import {onMount} from 'svelte';

    let count = 0;
    onMount(() => {
        const interval = setInterval(() => count++, 1000);
        return () => {
            clearInterval(interval);
        };
    });
</script>

<style>
    .App-header {
        background-color: #f9f6f6;
        color: #333;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: calc(10px + 2vmin);
    }
    .App-logo {
        height: 36vmin;
        pointer-events: none;
        margin-bottom: 3rem;
        animation: App-logo-pulse infinite 1.6s ease-in-out alternate;
    }
    @keyframes App-logo-pulse {
        from {
            transform: scale(1);
        }
        to {
            transform: scale(1.06);
        }
    }
</style>

<header class="bg-red-500 h24 flex justify-center items-center flex-col text-3xl">
    this is the header
</header>


<div class="App">
    <header class="App-header">
        <p class="App-logo" alt="logo">TEST</p>
        <p>Page has been open for <code>{count}</code> seconds.</p>
        <a class="App-link" href="https://svelte.dev" target="_blank" rel="noopener noreferrer">
            Learn Svelte
        </a>
    </header>

    <blockquote>
        <p><em>Yeah!! Milligram is amazing.</em></p>
    </blockquote>

    <form>
        <fieldset>
            <label for="nameField">Name</label>
            <input type="text" placeholder="CJ Patoilo" id="nameField">
            <label for="ageRangeField">Age Range</label>
            <select id="ageRangeField">
                <option value="0-13">0-13</option>
                <option value="14-17">14-17</option>
                <option value="18-23">18-23</option>
                <option value="24+">24+</option>
            </select>
            <label for="commentField">Comment</label>
            <textarea placeholder="Hi CJ …" id="commentField"></textarea>
            <div class="float-right">
                <input type="checkbox" id="confirmField">
                <label class="label-inline" for="confirmField">Send a copy to yourself</label>
            </div>
            <input class="button-primary" type="submit" value="Send">
        </fieldset>
    </form>

    <table>
        <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Height</th>
            <th>Location</th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td>Stephen Curry</td>
            <td>27</td>
            <td>1,91</td>
            <td>Akron, OH</td>
        </tr>
        <tr>
            <td>Klay Thompson</td>
            <td>25</td>
            <td>2,01</td>
            <td>Los Angeles, CA</td>
        </tr>
        </tbody>
    </table>
</div>