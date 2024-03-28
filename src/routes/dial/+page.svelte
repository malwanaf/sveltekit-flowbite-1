<script>
    import { SpeedDial, SpeedDialButton } from 'flowbite-svelte';
    import { ShareNodesSolid, PrinterSolid, DownloadSolid, FileCopySolid } from 'flowbite-svelte-icons';
  </script>
  
  <SpeedDial defaultClass="absolute end-0 border-2 rounded-full border-gray-300" trigger="click" color="light">
    <SpeedDialButton name="Share">
      <ShareNodesSolid class="w-5 h-5" />
    </SpeedDialButton>
    <SpeedDialButton name="Print">
      <PrinterSolid class="w-5 h-5" />
    </SpeedDialButton>
    <SpeedDialButton name="Download">
      <DownloadSolid class="w-5 h-5" />
    </SpeedDialButton>
    <SpeedDialButton name="Copy">
      <FileCopySolid class="w-5 h-5" />
    </SpeedDialButton>
  </SpeedDial>