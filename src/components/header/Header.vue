<template>
    <header class="header">
        <div class="header__content">
            <div class="header__nav">
                <div class="nav-bars">
                    <span class="material-symbols-outlined">menu</span>
                </div>
            </div>
            <div class="header__brand">
                <span>Budget Bee</span>
            </div>
            <div class="header__notification">
                <div class="notify">
                    <span class="material-symbols-outlined">notifications</span>
                    <div class="notify__counter">2</div>
                </div>
                
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style lang="scss" scoped>
    .header{
        display: flex;
        align-items: center;
        height: 70px;
        background: rgb(87,134,255);
        background: linear-gradient(17deg, rgba(87,134,255,1) 0%, rgba(51,157,255,1) 100%);

        &__content{
            display: flex;
            justify-content: space-between;
            padding: 0 20px;
            width: 100%;
        }

        &__nav{
            .nav-bars{
                color: #fff;
                cursor: pointer;
            }
        }
    }
    .notify{
        position: relative;
        color: #fff;
        cursor: pointer;

        &__counter{
            position: absolute;
            top: -3px;
            right: -3px;
            background: rgb(247, 25, 25);
            width: 18px;
            height: 18px;
            border-radius: 18px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: 700;
            font-size: 12px;
        }
    }
</style>