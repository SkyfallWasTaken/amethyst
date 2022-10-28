<script>
    import { exit as tauriExit } from '@tauri-apps/api/process';

    import PlayIcon from "svelte-feather-icons/src/icons/PlayIcon.svelte";
    import SettingsIcon from "svelte-feather-icons/src/icons/SettingsIcon.svelte";
    import KeyIcon from "svelte-feather-icons/src/icons/KeyIcon.svelte";
    import LogOutIcon from "svelte-feather-icons/src/icons/LogOutIcon.svelte";

    const iconSize = "20";

    async function exit() {
        await tauriExit()
    }
</script>

<ul class="menu bg-base-300 h-screen w-56 p-2">
    <li>
        <a href="/authentication">
            <KeyIcon size={iconSize} />
            Authentication
        </a>
    </li>
    <div class="divider m-0" />
    <li>
        <a href="/">
            <PlayIcon size={iconSize} />
            Instances
        </a>
    </li>
    <li>
        <a href="/settings">
            <SettingsIcon size={iconSize} />
            Settings
        </a>
    </li>
    <li class="mt-auto">
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a on:click={exit} on:keydown={exit} href="#">
            <LogOutIcon size={iconSize} />
            Exit
        </a>
    </li>
</ul>
