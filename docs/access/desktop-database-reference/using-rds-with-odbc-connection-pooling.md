---
title: Utilisation de RDS avec le regroupement de connexions ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ecba73414a120309758aa2fa37af6da15a7c220b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870365"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Utilisation de RDS avec le regroupement de connexions ODBC


**S’applique à**: Access 2013, Office 2013

Si vous utilisez une source de données ODBC, vous pouvez utiliser l'option de regroupement de connexions IIS (Internet Information Services) pour bénéficier d'une gestion haute performance de la charge client. Le regroupement de connexions est un gestionnaire de ressources pour les connexions, qui maintient l'état ouvert sur les connexions fréquemment utilisées.

Pour activer le regroupement de connexions, reportez-vous à la documentation IIS.

Veuillez noter que l’activation du regroupement connexion peut-être imposer au serveur web d’autres restrictions, comme indiqué dans la documentation de Microsoft Internet Information Services.

Pour assurer la stabilité du regroupement de connexions et bénéficier de performances optimales, vous devez configurer Microsoft SQL Server afin qu'il utilise la bibliothèque réseau de sockets TCP/IP.

Pour ce faire, vous devez :

  - configurer l'ordinateur SQL Server pour une utilisation des sockets TCP/IP ;

  - Configurer le serveur web pour une utilisation des Sockets TCP/IP.

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a>Configuration de l'ordinateur SQL Server pour une utilisation des sockets TCP/IP

Sur l'ordinateur SQL Server, exécutez le programme d'installation de SQL Server de sorte que la bibliothèque réseau de sockets TCP/IP soit utilisée lors des interactions avec la source de données.

**Pour spécifier la bibliothèque réseau de sockets TCP/IP sur l'ordinateur SQL Server**

**Dans Microsoft SQL Server 6.5 :**

1.  Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Installation de SQL Server**.

2.  Cliquez deux fois sur **Continuer**.

3.  Dans la boîte de dialogue **Microsoft SQL Server  Options**, sélectionnez **Modifier la prise en charge du réseau**, puis cliquez sur **Continuer**.

4.  Assurez-vous que la case à cocher **Sockets TCP/IP** est activée, puis cliquez sur **OK**.

5.  Cliquez sur **Continuer** pour terminer et quitter le programme d'installation.

**Dans Microsoft SQL Server 7.0 :**

1.  Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Serveur**.

2.  Sous l'onglet **Général** de la boîte de dialogue, cliquez sur **Ajouter**.

3.  Dans la boîte de dialogue **Ajouter une configuration de bibliothèque réseau**, cliquez sur **TCP/IP**.

4.  Dans les zones **Numéro de port** et **Adresse Proxy**, entrez le numéro de port et l'adresse proxy fournis par votre administrateur réseau.

5.  Cliquez sur **OK** pour terminer et quitter le programme d'installation.

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Configuration du serveur pour l’utilisation des Sockets TCP/IP web

Il existe deux options de configuration du serveur web pour utiliser des Sockets TCP/IP. Que faire dépend si tous les serveurs SQL sont accessibles à partir du serveur web, ou uniquement un serveur SQL Server spécifique est accessible à partir du serveur web.

Si tous les serveurs SQL sont accessibles à partir du serveur web, vous devez exécuter l’utilitaire de Configuration de Client SQL Server sur l’ordinateur serveur web. La procédure suivante modifie la bibliothèque réseau par défaut pour toutes les connexions SQL Server sont effectuées à partir de ce serveur web IIS à utiliser la bibliothèque réseau de Sockets TCP/IP.

**Pour configurer le serveur web (tous les serveurs SQL)**

**Pour Microsoft SQL Server 6.5 :**

1.  Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.

2.  Cliquez sur l'onglet **Net-Library**.

3.  Dans la zone **Réseau par défaut**, sélectionnez **Sockets TCP/IP**.

4.  Cliquez sur **Terminé** pour enregistrer les modifications et quitter l'utilitaire.

**Pour Microsoft SQL Server 7.0 :**

1.  Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire Réseau Client**.

2.  Cliquez sur l'onglet **Général**.

3.  Dans la zone **Bibliothèque réseau par défaut**, cliquez sur **TCP/IP**.

4.  Cliquez sur **OK** pour enregistrer les modifications et quitter l'utilitaire.

Si un serveur SQL Server spécifique est accessible à partir d’un serveur web, vous devez exécuter l’utilitaire de Configuration de Client SQL Server sur l’ordinateur serveur web. Pour modifier la bibliothèque réseau pour une connexion SQL Server spécifique, configurez le logiciel Client de SQL Server sur l’ordinateur serveur web comme suit.

**Pour configurer le serveur web (spécifique SQL Server)**

**Pour Microsoft SQL Server 6.5 :**

1.  Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 6.5**, puis cliquez sur **Utilitaire de configuration de client SQL Server**.

2.  Cliquez sur l'onglet **Avancé**.

3.  Dans la zone **Serveur**, tapez le nom du serveur auquel se connecter à l'aide de **sockets TCP/IP**.

4.  Dans la zone **Nom de DLL**, sélectionnez **Sockets TCP/IP**.

5.  Cliquez sur **Ajouter/Modifier**. Toutes les sources de données pointant vers ce serveur utiliseront désormais les sockets TCP/IP.

6.  Cliquez sur **Terminé**.

**Pour Microsoft SQL Server 7.0 :**

1.  Dans le menu **Démarrer**, pointez sur **Programmes**, sur **Microsoft SQL Server 7.0**, puis cliquez sur **Utilitaire de configuration de client**.

2.  Cliquez sur l'onglet **Général**.

3.  Cliquez sur **Ajouter**.

4.  Entrez l'alias du serveur dans la zone **Alias du serveur**. Dans la zone **Bibliothèques réseau**, cliquez sur **TCP/IP**. Dans la zone **Nom de l'ordinateur**, entrez le nom de l'ordinateur qui est à l'écoute des clients utilisant des sockets TCP/IP. Dans la zone **Numéro de port**, entrez le port d'écoute utilisé par le serveur SQL Server.

5.  Cliquez sur **OK**, puis sur **OK** à nouveau pour quitter l’utilitaire.

