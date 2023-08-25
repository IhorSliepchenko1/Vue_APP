<template>
    <form class="form">
        <div class="form__title">NFT Access</div>
        <div class="form__desc">
            Please fill your detail to access your account.
        </div>

        <InputElement title="Email" name="email" type="email" placeholder="Your Email" />
        <InputElement title="Password" name="password" type="password" placeholder="Your Password" />

        <div class="row">
            <CheckboxElement label="Remember me" />
            <a href="/">Forgot Password?</a>
        </div>
        <div class="form__btn">
            <ButtonElement class="btn _primary">Sign in</ButtonElement>
            <ButtonElement class="btn _secondary">
                <GoogleIcon />
                Sign in with Google
            </ButtonElement>
        </div>
        <div class="row _center">
            Don’t have an account? <a href="/">Sign up</a>
        </div>
    </form>
</template>

<script>
import ButtonElement from "./UI/Button/ButtonElement";
import GoogleIcon from "./icons/GoogleIcon";
import InputElement from "./UI/Input/InputElement";
import CheckboxElement from "./UI/Checkbox/CheckboxElement";


export default {
    components: {
        InputElement,
        CheckboxElement,
        ButtonElement,
        GoogleIcon
    }

};
</script>

<style lang="scss">
.form {
    max-width: 360px;
    margin: auto;

    &__btn {
        display: grid;
        gap: 16px;
        margin-top: 32px;
        margin-bottom: 20px;
    }

    &__title {
        color: #344054;
        font-family: Inter;
        font-size: 40px;
        font-weight: 700;
        letter-spacing: 0.4px;
        text-transform: capitalize;
        margin-bottom: 8px;
    }

    &__desc {
        color: #667085;
        font-family: Inter;
        font-size: 16px;
        font-weight: 400;
        line-height: 24px;
        margin-bottom: 56px;
    }
}


.btn {
    display: inline-flex;
    width: 100%;
    bottom: 0;
    outline: 0;
    cursor: pointer;
    border-radius: 8px;
    justify-content: center;
    align-items: center;

    &._primary {
        background: #5429ff;
        color: #fff;
        font-family: Inter;
        font-size: 16px;
        font-weight: 500;
        line-height: 20px;
        border: 0;
        padding: 12px 154px;
    }

    &._secondary {
        border: 1px solid #d0d5dd;
        color: #344054;
        font-family: Inter;
        font-size: 16px;
        font-style: normal;
        font-weight: 500;
        line-height: 20px;
        background: transparent;
        padding: 10px 90px;
    }
}
</style>
