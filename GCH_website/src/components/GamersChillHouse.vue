<template>
    <div class="hidden md:flex flex-row bg-white shadow-xl shadow-blue-500/50 rounded-b-lg">
      <div class="basis-1/2">
        <img alt="" class="float-left w-28 hidden xl:block" src="../assets/images/clan-logo.png" />
        <img alt="" class="float-right mx-5 w-48 hidden sm:block" src="../assets/images/10.png" />
      </div>
      <div class="basis-1/2">
        <h1 class="float-left font-honk text-5xl text-black w-fit mx-5 my-7">GamersChillHouse</h1>
        <img alt="" class="float-right w-28 hidden xl:block" src="../assets/images/clan-logo.png" />
      </div>
    </div>
    <div class="flex flex-row">
      <div class="basis-1/3 hidden md:block bg-gray-950 mr-5 shadow-lg shadow-blue-500/50">
        <div class="h-screen">
          <div class="non-scrollable-container h-full overflow-auto">
            <div class="scrollable-div max-h-full overflow-y-auto pb-28">
              <h1
                class="font-honk text-5xl text-black text-center border border-blue-600 mx-5 my-7"
              >
                <a target="_blank" href="https://warframe.market/">Warframe Market</a>
              </h1>
              <p class="text-center mx-8 text-white font-mono h-fit text-wrap text-xl">
                De link hierboven leidt je naar een site waar je in game items kan kopen en verkopen
                met platinum. Zo kan je bijvoorbeeld mods farmen om platinum te verdienen en daar
                kan je dan weer warframes van halen of andere mods van halen.
              </p>
              <h1 class="font-honk text-5xl text-black text-center mx-5 my-7">
                <button v-on:click="isHiddenDojo = !isHiddenDojo">Click for dojo</button>
              </h1>
              <img
                v-if="!isHiddenDojo"
                alt=""
                class="mx-auto h-96"
                src="../assets/images/screenshot-dojo-1.png"
              />
              <br />
              <img
                v-if="!isHiddenDojo"
                alt=""
                class="mx-auto h-96"
                src="../assets/images/screenshot-dojo-2.png"
              />
              <br />
              <img
                v-if="!isHiddenDojo"
                alt=""
                class="mx-auto h-96"
                src="../assets/images/screenshot-dojo-3.png"
              />
              <br />
              <img
                v-if="!isHiddenDojo"
                alt=""
                class="mx-auto h-96"
                src="../assets/images/screenshot-dojo-4.png"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="mx-auto sm:basis-1/3">
        <div class="h-screen">
          <div class="non-scrollable-container h-full overflow-auto">
            <div class="scrollable-div max-h-full overflow-y-auto pb-28">
              <h1 class="font-honk text-5xl text-black text-center mx-5 my-7">Messages</h1>
              <div class="text-center">
                <h5 class="text-xl text-white">Title:</h5>
                <textarea
                  v-model="title"
                  type="text"
                  class="form-control rounded-lg text-center text-white bg-blue-900"
                ></textarea>
                <h5 class="text-xl text-white">User:</h5>
                <textarea
                  v-model="user"
                  type="text"
                  class="form-control rounded-lg text-center text-white bg-blue-900"
                ></textarea>
                <h5 class="text-xl text-white">Content:</h5>
                <textarea
                  v-model="content"
                  type="text"
                  class="form-control rounded-lg text-center text-white bg-blue-900"
                ></textarea>
                <br />
                <button
                  @click="submitDocument"
                  class="btn btn-primary rounded-lg text-white mt-4 px-5 p-2 bg-lime-600 mb-3"
                >
                  Submit
                </button>
              </div>
              <div v-for="(item, index) in documents" :key="index">
                <div class="bg-blue-900 shadow-lg shadow-blue-500/50 rounded-lg mb-4 p-1 mx-5">
                  <div
                    class="text-center text-white text-wrap truncate font-mono h-fit max-w-sm sm:max-w-xl"
                  >
                    <h1 class="text-2xl">
                      Title -
                      {{ item.title }}
                    </h1>
                    <h2 class="text-xl">
                      User -
                      {{ item.user }}
                    </h2>
                    <p class="text-lg">
                      {{ item.content }}
                    </p>
                  </div>
                </div>
                <div v-if="!item.hideFunctions">
                  <div class="text-center flex justify-center mb-4">
                    <div class="pointer" @click="updateDocument(index)">
                      <span class="bg-yellow-500 px-5 p-1.5 rounded-lg text-white mr-5">Edit</span>
                    </div>
                    <div class="pointer" @click="deleteDocument(index)">
                      <span class="bg-red-500 px-5 p-1.5 rounded-lg text-white mr-5">Delete</span>
                    </div>
                  </div>
                </div>
                <div v-else class="text-center">
                  Dit bericht kan niet aangepast of verwijderd worden.
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="basis-1/3 hidden md:block bg-gray-950 shadow-lg shadow-blue-500/50">
        <div class="h-screen">
          <div class="non-scrollable-container h-full overflow-auto">
            <div class="scrollable-div max-h-full overflow-y-auto pb-28">
              <h1 class="font-honk text-5xl text-black text-left mx-5 my-7">
                <button v-on:click="isHiddenClanInfo = !isHiddenClanInfo">
                  Click for clan info
                </button>
              </h1>
              <img
                v-if="!isHiddenClanInfo"
                alt=""
                class="mx-auto h-96"
                src="../assets/images/clan-info.png"
              />
              <h1 class="font-honk text-5xl text-black text-left mx-5 my-7">Admins</h1>
              <ul class="text-left mx-8 text-white font-mono h-fit text-wrap text-2xl">
                <li class="list-disc list-inside">Quin</li>
                <li class="list-disc list-inside">Marcel</li>
                <li class="list-disc list-inside">Lucas</li>
              </ul>
              <h1 class="font-honk text-5xl text-black text-left mx-5 mt-7">Discord promo</h1>
              <h1 class="font-mono text-2xl text-left text-blue-600 underline mx-5 pb-5">
                <a target="_blank" href="https://discord.gg/VcBkxTPYaR">Discord invite link</a>
              </h1>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import firebaseApp from '@/firebase'
import {
  getFirestore,
  collection,
  addDoc,
  updateDoc,
  doc,
  deleteDoc,
  getDocs
} from 'firebase/firestore'

export default {
  name: 'DocumentApp',
  data() {
    return {
      title: '',
      user: '',
      content: '',
      updatedDocument: null,
      documents: [],
      isHiddenClanInfo: true,
      isHiddenDojo: true
    }
  },
  created() {
    this.fetchDocuments()
  },
  methods: {
    async fetchDocuments() {
      const db = getFirestore(firebaseApp);
      const querySnapshot = await getDocs(collection(db, 'messages'));

      this.documents = querySnapshot.docs.map((doc) => {
        const data = { id: doc.id, ...doc.data() };

        if (data.user === 'Sjedei') {
          return { ...data, hideFunctions: true };
        }
        return { ...data, hideFunctions: false };
      });
    },
    async submitDocument() {
      if (this.title.length === 0 || this.user.length === 0 || this.content.length === 0) return

      const db = getFirestore(firebaseApp)
      if (this.updatedDocument === null) {
        await addDoc(collection(db, 'messages'), {
          title: this.title,
          user: this.user,
          content: this.content
        })
      } else {
        await updateDoc(doc(db, 'messages', this.updatedDocument), {
          title: this.title,
          user: this.user,
          content: this.content
        })
        this.updatedDocument = null
      }
      this.title = ''
      this.user = ''
      this.content = ''
      await this.fetchDocuments()
    },
    updateDocument(index) {
      const document = this.documents[index]
      this.title = document.title
      this.user = document.user
      this.content = document.content
      this.updatedDocument = document.id
    },
    async deleteDocument(index) {
      const document = this.documents[index]
      const db = getFirestore(firebaseApp)
      await deleteDoc(doc(db, 'messages', document.id))
      await this.fetchDocuments()
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/sass/app.scss';
</style>
