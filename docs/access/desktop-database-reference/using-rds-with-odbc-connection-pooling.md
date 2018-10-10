---
title: Utilisation de RDS avec le regroupement de connexions ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7baaf81d7a5d6a91416ea5baf8ba57745612740e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469436"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Utilisation de RDS avec le regroupement de connexions ODBC


**S’applique à**: Access 2013 | Office 2013

Si vous utilisez une source de données ODBC, vous pouvez utiliser l'option de regroupement de connexions IIS (Internet Information Services) pour bénéficier d'une gestion haute performance de la charge client. Le regroupement de connexions est un gestionnaire de ressources pour les connexions, qui maintient l'état ouvert sur les connexions fréquemment utilisées.

Pour activer le regroupement de connexions, reportez-vous à la documentation IIS.

Il est à noter que l'activation du regroupement de connexions est susceptible d'imposer au serveur Web d'autres restrictions, comme le mentionne la documentation Microsoft IIS.

Pour assurer la stabilité du regroupement de connexions et bénéficier de performances optimales, vous devez configurer Microsoft SQL Server afin qu'il utilise la bibliothèque réseau de sockets TCP/IP.

Pour ce faire, vous devez :

  - configurer l'ordinateur SQL Server pour une utilisation des sockets TCP/IP ;

  - configurer le serveur Web pour une utilisation des sockets TCP/IP.

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

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Configuration du serveur Web pour une utilisation des sockets TCP/IP

Pour configurer le serveur Web en vue d'une utilisation des sockets TCP/IP, vous devez utiliser l'une ou l'autre des deux options disponibles, selon que l'accès à tous les serveurs SQL Server s'effectue à partir du serveur Web, ou que ce dernier n'accède qu'à un seul serveur SQL Server spécifique.

Si l'accès à tous les serveurs SQL Server s'effectue à partir du serveur Web, vous devez exécuter l'utilitaire de configuration de client SQL Server sur le serveur Web. La procédure suivante modifie la bibliothèque réseau par défaut pour toutes les connexions SQL Server établies à partir de ce serveur Web IIS en vue de l'utilisation de la bibliothèque réseau de sockets TCP/IP.

**Pour configurer le serveur Web (tous les serveurs SQL Server)**

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

Si l'accès à un serveur SQL Server spécifique s'effectue à partir d'un serveur Web, vous devez exécuter l'utilitaire de configuration de client SQL Server sur le serveur Web. Pour modifier la bibliothèque réseau pour une connexion SQL Server spécifique, configurez le logiciel Client SQL Server sur le serveur Web comme indiqué ci-dessous.

**Pour configurer le serveur Web (serveur SQL Server spécifique)**

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

