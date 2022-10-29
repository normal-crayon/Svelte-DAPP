<script>
    import {username, user} from './user';

    function signout(){
        user.leave();
        username.set('');
    }
</script>

<header>
    <h1>Svelte App</h1>
    {#if username}
    <div class="user-bio">
        <span>Hello<strong>{$username}</strong></span>
        <img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt="avatar" />

    </div>
    <button class="signout-button" on:click="{signout}">Signout</button>
    {:else}

    <h3>Svelte Chat </h3>
    <h4>Powered by GUN</h4>
    {/if}
</header>