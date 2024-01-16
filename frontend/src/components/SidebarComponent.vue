<!-- <template>
  <div class="sidebar">
    <div class="sidebar-header">
      CLINIQUE HANNAH
    </div>
    <div class="menu-item" @click="toggleSubMenu(0)">
      Accueil
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 0 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(1)">
      Patient
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 1 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(2)">
      Consultation
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 2 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(2)">
      Document
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 2 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(2)">
      Planning
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 2 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(2)">
      Facturation 
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 2 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(2)">
      Honoraire des Gardes
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 2 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
    <div class="menu-item" @click="toggleSubMenu(2)">
      Honoraires par taux
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === 2 }">
        <div class="sub-menu-item">Sous-tâche 1</div>
        <div class="sub-menu-item">Sous-tâche 2</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  background-color: #1E3856;
  color: white;
  width: 250px;
  height: calc(100vh - 20px);
  display: flex;
  flex-direction: column;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.sidebar-header {
  background-color: #0F2340;
  padding: 20px;
  font-size: 24px;
  text-align: center;
  border-bottom: 1px solid #4F7A9C;
  font-weight: 600;
}

.menu-item {
  position: relative;
  cursor: pointer;
  margin-bottom: 10px; /* Ajout de marge inférieure pour espacement */
}

.sub-menu {
  display: none;
}

.sub-menu.show {
  display: block;
}

.sub-menu-item {
  padding: 10px 20px;
  font-size: 16px;
  border-bottom: 1px solid #4F7A9C;
  transition: background-color 0.3s ease;
}

.sub-menu-item:last-child {
  border-bottom: none;
}

.sub-menu-item:hover {
  background-color: #144C73;
}
</style>

<script>
export default {
  data() {
    return {
      activeSubMenuIndex: -1
    };
  },
  methods: {
    toggleSubMenu(index) {
      this.activeSubMenuIndex = this.activeSubMenuIndex === index ? -1 : index;
    }
  }
};
</script> -->

<!-- <template>
  <div class="sidebar">
    <div class="sidebar-header">
      <span>MENU</span>
      CLINIQUE HANNAH
    </div>
    <div v-for="(menuItem, index) in menuItems" :key="index" class="menu-item" @click="toggleSubMenu(index)">
      <FontAwesomeIcon :icon="menuItem.icon" /> {{ menuItem.label }}
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === index }">
        <div v-for="(subItem, subIndex) in menuItem.subMenu" :key="subIndex" class="sub-menu-item">
          {{ subItem }}
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  background-color: #1E3856;
  color: white;
  width: 250px;
  height: calc(100vh - 20px);
  display: flex;
  flex-direction: column;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  box-shadow: 2px 0px 5px rgba(0, 0, 0, 0.2); /* Ajout d'une légère ombre à la barre latérale */
}

.sidebar-header {
  background-color: #0F2340;
  padding: 10px;
  font-size: 17px;
  text-align: center;
  border-bottom: 1px solid #4F7A9C;
  font-weight: 600;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 23px; 
}

.sidebar-header span {
  font-size: 16px;
  margin-bottom: 5px;
}

.menu-item {
  position: relative;
  cursor: pointer;
  margin-bottom: 60px;
  font-size: 21px;
  margin-left: 12px
}

.sub-menu {
  display: none;
}

.sub-menu.show {
  display: block;
}

.sub-menu-item {
  padding: 10px 20px;
  font-size: 16px;
  border-bottom: 1px solid #4F7A9C;
  transition: background-color 0.3s ease;
}

.sub-menu-item:last-child {
  border-bottom: none;
}

.sub-menu-item:hover {
  background-color: #144C73;
}
</style>

<script>
import { library } from '@fortawesome/fontawesome-svg-core';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faHome, faUser, faSearch, faFile, faCalendar, faMoneyBill, faClock, faPercent,} from '@fortawesome/free-solid-svg-icons';
library.add(faHome, faUser, faSearch, faFile, faCalendar, faMoneyBill, faClock, faPercent,);

export default {
  components: {
    FontAwesomeIcon,
  },
  data() {
    return {
      activeSubMenuIndex: -1,
      menuItems: [
        { label: "Accueil", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'home'] },
        { label: "Patient", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'user'] },
        { label: "Consultation", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'search']},
        { label: "Documents", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'file']},
        { label: "Planning", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'calendar'] },
        { label: "Facturation", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'money-bill'] },
        { label: "Honoraire des Gardes", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'clock'] },
        { label: "Honoraires par taux", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'percent'] },
        // Ajoutez le reste des éléments de menu ici
      ]
    };
  },
  methods: {
    toggleSubMenu(index) {
      this.activeSubMenuIndex = this.activeSubMenuIndex === index ? -1 : index;
    }
  }
};
</script> -->

<template>
  <div class="sidebar">
    <div class="sidebar-header">
      <span>MENU</span>
      CLINIQUE HANNAH
    </div>
    <div v-for="(menuItem, index) in menuItems" :key="index" :class= "{'menu-item' : true , 'long-label': menuItem.label.length > 20 }" @click="toggleSubMenu(index)">
      <FontAwesomeIcon :icon="menuItem.icon" class="icon" />
      {{ menuItem.label }}
      <div class="sub-menu" :class="{ show: activeSubMenuIndex === index }">
        <div v-for="(subItem, subIndex) in menuItem.subMenu" :key="subIndex" class="sub-menu-item">
          {{ subItem }}
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  background-color: #1E3856;
  color: white;
  width: 250px;
  height: calc(100vh - 20px);
  display: flex;
  flex-direction: column;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  box-shadow: 2px 0px 5px rgba(0, 0, 0, 0.2);
}

.sidebar-header {
  background-color: #0F2340;
  padding: 10px;
  font-size: 17px;
  text-align: center;
  border-bottom: 1px solid #4F7A9C;
  font-weight: 600;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 23px; 
}

.sidebar-header span {
  font-size: 16px;
  margin-bottom: 5px;
}

.menu-item {
  position: relative;
  cursor: pointer;
  margin-bottom: 60px;
  font-size: 21px;
  margin-left: 12px;
  display: flex;
  align-items: center;
}

.menu-item.long-label {
  flex-direction: column;
  align-items: flex-start;
}

.menu-item .icon {
  margin-right: 8px; /* Ajustez l'espace entre l'icône et le libellé selon vos préférences */
}

.menu-item:hover {
  background-color: #144C73;
}

.sub-menu {
  display: none;
}

.sub-menu.show {
  display: block;
}

.sub-menu-item {
  padding: 10px 20px;
  font-size: 16px;
  border-bottom: 1px solid #4F7A9C;
  transition: background-color 0.3s ease;
}

.sub-menu-item:last-child {
  border-bottom: none;
}

.sub-menu-item:hover {
  background-color: #144C73;
}
</style>

<script>
import { library } from '@fortawesome/fontawesome-svg-core';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faHome, faUser, faSearch, faFile, faCalendar, faMoneyBill, faClock, faPercent,} from '@fortawesome/free-solid-svg-icons';
library.add(faHome, faUser, faSearch, faFile, faCalendar, faMoneyBill, faClock, faPercent,);

export default {
  components: {
    FontAwesomeIcon,
  },
  data() {
    return {
      activeSubMenuIndex: -1,
      menuItems: [
        { label: "Accueil", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'home'] },
        { label: "Patient", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'user'] },
        { label: "Consultation", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'search']},
        { label: "Documents", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'file']},
        { label: "Planning", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'calendar'] },
        { label: "Facturation", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'money-bill'] },
        { label: "Honoraire des Gardes", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'clock'] },
        { label: "Honoraires par taux", subMenu: ["Sous-tâche 1", "Sous-tâche 2"], icon: ['fas', 'percent'] },
        // Ajoutez le reste des éléments de menu ici
      ]
    };
  },
  methods: {
    toggleSubMenu(index) {
      this.activeSubMenuIndex = this.activeSubMenuIndex === index ? -1 : index;
    }
  }
};
</script>