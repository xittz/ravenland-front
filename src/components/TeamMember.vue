<template>
    <div class="member">
        <div>
            <img class="member-photo" :src="member.img">
        </div>
        <div>
            <p class="text name">
                {{ member.name }}
            </p>
            <p class="text position">
                {{ member.position }}
            </p>
            <p class="text description">
                {{ member.text }}
            </p>
        </div>
        <div class="socials">
            <a v-if="member.socials.linkedin != null" 
               :href="member.socials.linkedin">
               <i class="fab fa-linkedin-in"></i>
            </a>

            <a v-if="member.socials.twitter != null"
               :href="member.socials.twitter">
                <i class="fab fa-twitter"></i>
            </a>
            <a v-if="member.socials.github != null"
               :href="member.socials.linkedin">
                <i class="fab fa-github"></i>
            </a>
        </div>
    </div>
</template>

<script>

export default {
  name: 'TeamMember',
  props: ['member']
}
</script>

<style scoped>

.member {
    padding-bottom: 30px;
}

.member-photo {
  padding: 0;
  border-radius: 50%;
}

.fab {
    font-size: 24px;
    color: white;
    margin: 10px;
}

.fab:hover {
    color:#f15b22;
}

.socials {
    padding-top: 20px;
}

.text {
    color: white;
    margin: 0;
}

.position {
    font-size: 24px;
    margin-bottom: 0px;
}


.name {
    font-size: 2rem;
}

.description {
    font-size: 24px;
}
</style>
