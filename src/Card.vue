<template>
    <div>
        <div class="card">
            <img
                alt=""
                class="card-image"
                src="https://static.overlay-tech.com/assets/0a6b7f31-7bca-4171-a030-400f84d45bba.png"
            />
            <div class="profile">
                <div class="infos">
                    <img
                        alt=""
                        class="ellipse-21"
                        src="https://static.overlay-tech.com/assets/b58a2a75-8aec-4b4d-9a52-84736d40af54.png"
                    />
                    <h3 class="profile-name">{{ profileName }}</h3>
                </div>
                <button class="like">
                    <img alt="" src="https://static.overlay-tech.com/assets/d16821b2-8a2a-4486-8558-8becb27e0c23.svg" />
                </button>
            </div>
            <p class="description">{{ description }}</p>
            <Button class="button-button" />
        </div>
    </div>
</template>
<script>
import { Button } from './components';
export default {
    name: 'CardWithButton',
    wwDefaultContent: {},
    components: { Button },
    props: {
        profileName: { type: String, default: 'Girafe' },
        description: {
            type: String,
            default: "Hi, I'm a card with a caption and a like icon. And I'm responsive ;)",
        },
    },
};
</script>
<style lang="scss" scoped>
.card {
    background-color: white;
    border-radius: 12px;
    padding: 22px;
    box-shadow: 4px 4px 0px 0 black;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    border: 2px solid black;
}
.card-image {
    width: calc(100% - 4px);
    height: 211px;
    margin-bottom: 16px;
    border: 2px solid black;
    border-radius: 8px;
    object-fit: cover;
}
.profile {
    margin-bottom: 16px;
    padding: 1px 0;
    align-self: stretch;
    position: relative;
}
.infos {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
}
.ellipse-21 {
    width: 36px;
    height: 36px;
    margin-right: 16px;
    border: 2px solid black;
    border-radius: 50%;
}
.profile-name {
    color: black;
    flex: 1;
}
.like {
    padding: 10px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    position: absolute;
    right: 0;
    top: 0;
    cursor: pointer;
}
.description {
    color: black;
    width: 100%;
    margin-bottom: 16px;
}
.button-button {
    width: 155px;
}
</style>
