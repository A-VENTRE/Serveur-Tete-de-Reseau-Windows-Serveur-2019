   <h1>TP Serveur Tête de Réseau Windows Server 2019</h1>
   <h2>Description du Projet</h2>
    <p>Ce projet a pour objectif la configuration d'un serveur tête de réseau sous Windows Server 2019, incluant les services essentiels tels que DNS, DHCP, et Active Directory. Ce serveur permet de gérer efficacement les ressources réseau, de sécuriser les communications et de garantir une infrastructure fiable.</p>
    
   <h2>Table des Matières</h2>
    <ul>
        <li><a href="#introduction">Introduction</a></li>
        <li><a href="#preparation">Préparation de l'Environnement</a></li>
        <li><a href="#installation">Installation des Rôles Principaux</a></li>
        <li><a href="#configuration">Configuration des Services</a>
            <ul>
                <li><a href="#dns-options">Options DNS</a></li>
                <li><a href="#dns-configuration">Configuration du DNS</a></li>
                <li><a href="#dhcp-installation">Installation du DHCP</a></li>
            </ul>
        </li>
        <li><a href="#gestion-utilisateurs">Gestion des Utilisateurs et Groupes</a></li>
        <li><a href="#tests">Tests de Fonctionnement</a></li>
        <li><a href="#conclusion">Conclusion</a></li>
    </ul>

   <h2 id="introduction">Introduction</h2>
    <p>En tant que technicien réseau, la maîtrise des services tels que DNS, DHCP et Active Directory est cruciale pour assurer le bon fonctionnement d'une infrastructure informatique. Ce TP aborde l'installation et la configuration de ces services sous Windows Server 2019.</p>

   <h2 id="preparation">Préparation de l'Environnement</h2>
    <p>Avant de commencer l'installation des rôles, nous avons préparé le serveur :</p>
    <ul>
        <li>Renommage du serveur (<code>SRV10-104</code>) selon la convention de nommage.</li>
        <li>Configuration de l'adresse IP : <code>10.0.111.1</code> avec une passerelle <code>10.0.111.254</code> et les DNS <code>172.31.1.4</code> et <code>9.9.9.9</code>.</li>
    </ul>

  <h2 id="installation">Installation des Rôles Principaux</h2>
   <h3 id="dns-options">Installation d'Active Directory</h3>
    <p>La première étape a été l'installation d'Active Directory, qui est essentielle avant d'installer DNS et DHCP.</p>

   <h3>Options DNS</h3>
    <p>Une fois Active Directory installé, nous avons configuré une nouvelle forêt (<code>DOMADUT111.peda</code>) pour structurer notre environnement.</p>

   <h3 id="dhcp-installation">Installation du DHCP</h3>
   <p>Après la configuration du DNS, le service DHCP a été installé pour permettre une attribution dynamique des adresses IP.</p>

   <h2 id="configuration">Configuration des Services</h2>
    <h3 id="dns-configuration">Configuration du DNS</h3>
    <p>Nous avons choisi une configuration basique de DNS pour une résolution efficace des noms sur le réseau local.</p>

   <h3>Installation du DHCP</h3>
    <p>Le DHCP a été configuré pour deux étendues :</p>
    <ul>
        <li><strong>LAN0</strong> pour les tests internes.</li>
        <li><strong>LAN2</strong> pour une utilisation réelle.</li>
    </ul>

   <h2 id="gestion-utilisateurs">Gestion des Utilisateurs et Groupes</h2>
    <p>Nous avons mis en place une gestion des utilisateurs via Active Directory, en créant des comptes distincts pour chaque administrateur, incluant un compte à privilèges limités et un compte d'administration.</p>

   <h2 id="tests">Tests de Fonctionnement</h2>
    <p>Différents tests ont été effectués pour vérifier le bon fonctionnement des services DNS et DHCP :</p>
    <ul>
        <li>Test de <code>ping</code> pour vérifier la connectivité.</li>
        <li><code>nslookup</code> pour la résolution DNS.</li>
        <li>Connexion des clients au domaine pour tester les échanges.</li>
    </ul>

   <h2 id="conclusion">Conclusion</h2>
    <p>Ce projet a permis de maîtriser la gestion d'un serveur Windows 2019 en configurant les rôles DNS, DHCP et Active Directory. Les tests effectués ont confirmé la bonne intégration des services et la disponibilité du réseau pour les utilisateurs.</p>

   <h2>Ressources Utiles</h2>
    <ul>
        <li><a href="https://www.it-connect.fr/serveur-de-fichiers-les-permissions-ntfs-et-de-partage/">IT-Connect - Permissions NTFS et Partage</a></li>
        <li><a href="https://learn.microsoft.com/fr-fr/windows-server/get-started/whats-new-windows-server-2025">Learn Microsoft - Nouveautés de Windows Server 2025</a></li>
    </ul>
</body>
</html>

