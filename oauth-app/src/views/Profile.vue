<template>
    <div class="user-container">
        <div class="profile">
            <img class="profile-picture" :src="$auth.user.picture" alt="Profile Picture"/>
            <h2 class="user-name">{{ $auth.user.name }}</h2>
            <h5 class="user-email">{{ $auth.user.email }}</h5>
        </div>
        <div class="user-info">
            <pre>{{ JSON.stringify($auth.user, null, 2) }}</pre>
        </div>
    </div>
</template>

<style>
.user-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px;
}

.profile {
    text-align: center;
    margin-bottom: 20px;
    border: 1px solid #ccc;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
}

.profile-picture {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 10px;
}

.user-name {
    font-size: 1.5rem;
    margin-bottom: 5px;
}

.user-email {
    font-size: 1rem;
    color: #555;
}

.user-info {
    width: 100%;
    padding: 10px;
    background-color: #f9f9f9;
    border-radius: 10px;
    box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}
</style>
