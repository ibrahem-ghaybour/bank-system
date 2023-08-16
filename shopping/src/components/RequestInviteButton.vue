<template>
  <button id="requestInvite" @click="$router.push('/login')">Request Invite</button>
</template>

<style scoped>
button {
  padding: 10px 35px;
  border: none;
  border-radius: 20px;
  cursor: pointer;
  background: linear-gradient(to left, hsl(136, 65%, 51%), hsl(192, 70%, 51%));
  color: #fff;
  font-size: 18px;
}
button:hover {
  background: linear-gradient(to left, hsl(136, 85%, 65%), hsl(192, 76%, 65%));
}
@media ((max-width: 910px)  and (min-width: 800px )) {
  button {
    padding: 10px 20px;
    font-size: 15px;
  }
}
@media ((max-width: 800px)  and (min-width: 700px )) {
  button {
    padding: 10px 17px;
    font-size: 14px;
  }
}
@media ((max-width: 700px)  and (min-width: 620px )) {
  button {
    padding: 10px 15px;
    font-size: 13px;
  }
}
@media ((max-width: 620px) and (min-width:520px)) {
  button {
    padding: 10px 10px;
    font-size: 12px;
  }
}
</style>
