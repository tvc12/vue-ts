<template>
  <div>
    <ul v-for="value in statusCodes" :key="value.statusCode">
      <li>
        {{ value.displayName }}
      </li>
      <img :src="value.url" />
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HttpStatusCode from '@/modal/http_status_code';

export default class ListingImage extends Vue {
  statusCodes: HttpStatusCode[] = [
    { statusCode: '100', displayName: 'Continue', url: 'https://http.cat/101' },
    { statusCode: '200', displayName: 'Ok', url: 'https://http.cat/200' },
    { statusCode: '201', displayName: 'Created', url: 'https://http.cat/201' },
    { statusCode: '202', displayName: 'Accepted', url: 'https://http.cat/202' },
    { statusCode: '204', displayName: 'No Content', url: 'https://http.cat/204' },
    { statusCode: '207', displayName: 'Multi-Status', url: 'https://http.cat/207' },
    { statusCode: '300', displayName: 'Multiple Choices', url: 'https://http.cat/300' },
  ];
}
</script>
