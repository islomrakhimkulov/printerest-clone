<template>
  <v-container>
      <stack :column-min-width="280" :gutter-width="10" :gutter-height="8">
      <stack-item v-for="(item, i) in items" :key="i">
        <ImageCard 
        :url="item.url" 
        :meta="{name: item.name, 
        occupation: item.occupation,
        profileImageUrl: item.profileImageUrl,
        }"
        />
      </stack-item>
    </stack>
  </v-container>
</template>

<script>
import { Stack, StackItem } from "vue-stack-grid";
import ImageCard from "@/components/ImageCard.vue";
export default {
    name: "HomePage",
    components: { 
        Stack, StackItem,ImageCard
    },
    data: () => ({
        
        items: [
            {
                url: "https://images.unsplash.com/photo-1639654655546-68bc1f21e9e3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTg3fHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Davlat G'aniyev",
                occupation: "Project Manager",
                profileImageUrl: "https://images.unsplash.com/photo-1531427186611-ecfd6d936c79?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8cHJvZmlsZSUyMGltZyUyMHVybHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1640329767000-c9e98b19b24c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTI0fHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Islom Rakhimkulov",
                occupation:"Frontend Software Engineer",
                profileImageUrl: "https://images.unsplash.com/photo-1520592978680-efbdeae5d036?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8OTV8fHByb2ZpbGUlMjBpbWclMjB1cmx8ZW58MHx8MHx8&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1642354845684-8aeca235313c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjExfHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Javlonbek Kakhramonov",
                occupation:"Software Engineer",
                 profileImageUrl: "https://images.unsplash.com/photo-1503235930437-8c6293ba41f5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8cHJvZmlsZSUyMGltZyUyMHVybHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1589646557498-9b4b6d2edd48?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTExfHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Baxtiyor Begmatov",
                occupation: "Android Developer",
                 profileImageUrl: "https://images.unsplash.com/photo-1492562080023-ab3db95bfbce?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjQxfHxwcm9maWxlJTIwaW1nJTIwdXJsfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1481201779555-88fcea2968ca?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTI2fHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Sardor Nurov",
                occupation: "UI/UX Graphic Designer",
                 profileImageUrl: "https://images.unsplash.com/photo-1521341957697-b93449760f30?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Njl8fHByb2ZpbGUlMjBpbWclMjB1cmx8ZW58MHx8MHx8&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1640579809686-119e4a01b3b8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTk1fHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Javohir Urinov",
                occupation: "Backend Developer",
                 profileImageUrl: "https://images.unsplash.com/photo-1520611980017-9562f7d6dc82?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8ODd8fHByb2ZpbGUlMjBpbWclMjB1cmx8ZW58MHx8MHx8&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1642748355137-ceb55adc757e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTc5fHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Javohir Bozorov",
                occupation: "Frontend Developer",
                 profileImageUrl: "https://images.unsplash.com/photo-1521132293557-5b908a59d1e1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjAzfHxwcm9maWxlJTIwaW1nJTIwdXJsfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1616666739878-a53a829935ce?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTQxfHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Aslbek",
                occupation:" Copywriter",
                 profileImageUrl: "https://images.unsplash.com/photo-1536620303020-d49916c8634b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTgwfHxwcm9maWxlJTIwaW1nJTIwdXJsfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=400&q=60",
            },
            { 
                url: "https://images.unsplash.com/photo-1642767302089-4077da521476?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjAwfHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Aziz",
                occupation:"UI/UX and Frontend Developer ",
                 profileImageUrl: "https://images.unsplash.com/photo-1517819206436-716454919893?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NjV8fHByb2ZpbGUlMjBpbWclMjB1cmx8ZW58MHx8MHx8&auto=format&fit=crop&w=400&q=60",
            },
            {
                url: "https://images.unsplash.com/photo-1620480814072-c90d676a4538?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjA4fHx1emJla2lzdGFufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
                name: "Aziz",
                occupation:"Backend Developer",
                 profileImageUrl: "https://images.unsplash.com/photo-1561893836-adae6b766f82?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjg2fHxwcm9maWxlJTIwaW1nJTIwdXJsfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=400&q=60",
            },
        ]
    }),
}
</script>

<style>

</style>