<template>
    <div class="topline">
        <topline>
            <template #headline>
                <div class="icon">
                    <icon name="home" />
                </div>
            </template>
            <template #content>
                <ul class="stories">
                    <li class="stories-item" v-for="story in stories" :key="story.id">
                        <story-user-item
                            :avatar="story.avatar"
                            :username="story.username"
                            @onPress="handlePress(story.id)"
                        />
                    </li>
                </ul>
            </template>
        </topline>
    </div>
</template>

<script>
import stories from './data.json'
import { topline } from '../../components/topline'
import { icon } from '../../icons'
import { storyUserItem } from '../../components/storyUserItem'
export default {
  name: 'feeds',
  components: {
    topline,
    icon,
    storyUserItem
  },
  data () {
    return {
      stories
    }
  }
}
</script>

<style lang="scss" scoped src="./feeds.scss"></style>
