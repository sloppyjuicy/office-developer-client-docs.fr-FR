---
title: Message Gestion des téléchargements pour les comptes POP3
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: Cette section décrit comment le fournisseur POP3 de Outlook utilise l'historique de la liste d'ID Unique (UIDL) sur un compte POP3 pour identifier les messages que le fournisseur a téléchargé ou supprimés du serveur POP3, pour éviter le téléchargement de plusieurs fois le même message.
ms.openlocfilehash: b878c551884d8e9a0bd7f85d6f1b5832a6fa8548
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584786"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Message Gestion des téléchargements pour les comptes POP3

Cette section décrit comment le fournisseur POP3 de Outlook utilise l'historique de la liste d'ID Unique (UIDL) sur un compte POP3 pour identifier les messages que le fournisseur a téléchargé ou supprimés du serveur POP3, pour éviter le téléchargement de plusieurs fois le même message.
  
## <a name="introduction-to-pop"></a>Introduction aux POP

Le protocole POP (Post Office) spécifie un protocole de couche d'application pour un client de messagerie tel que Outlook télécharger des messages électroniques à partir d'un serveur de messagerie. Il permet à un utilisateur télécharger une copie d'un message électronique à un périphérique local (par exemple, un ordinateur ou un téléphone intelligent) et laisser une copie sur le serveur ou le supprimer. Le protocole prend en charge qu'un seul client de messagerie d'être connecté à la boîte aux lettres à la fois. Il indique uniquement comment récupérer, mais pas envoyer des messages e-mail à partir du serveur de messagerie. Lors de l'utilisation de POP, un client de messagerie en général a vérifier les nouveaux messages électroniques, se connecte au serveur de messagerie pour que la quantité de temps nécessaire pour télécharger les nouveaux messages et ne reste pas connecté au serveur pour obtenir des notifications de nouveau courrier. POP prend en charge uniquement les messages électroniques, mais pas autres types d'éléments tels que des contacts et des rendez-vous, sauf si elles sont encapsulées dans un message électronique. POP3 est la version 3 du protocole.
  
Pour un compte POP, les messages sont identifiées par des identificateurs uniques (UID). Client de messagerie électronique qui conserve les messages sur le serveur utilise la commande UIDL pour récupérer la carte UIDL qui associe chaque message a été remis à la boîte aux lettres à son UID. Le client obtient également l'historique de la commande UIDL pour les messages qui ont été téléchargés ou supprimés de la boîte de réception sur ce client. En fonction de l'historique de la commande UIDL, le client peut déterminer quels messages sont nouveaux et qu'il doivent être téléchargés.

- Localisation de l’historique de téléchargement des messages pour un compte [POP3](locating-the-message-download-history-for-a-pop3-account.md): cette rubrique décrit comment un client de messagerie accède à la propriété [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) pour obtenir l’historique UIDL des messages dans la boîte de réception du client d’un compte POP3. 
    
- L’historique de téléchargement des messages pour un compte [POP3](parsing-the-message-download-history-for-a-pop3-account.md): cette rubrique décrit comment l’objet BLOB POP3 qui représente l’historique UIDL des messages dans la boîte de réception du client d’un compte POP3, afin d’identifier les messages qui ont été téléchargés ou supprimés sur ce compte.
    
## <a name="see-also"></a>Voir aussi

- [Gestion des comptes Outlook](outlook-account-management.md)    
- [Localisation de l'historique de téléchargement des messages pour un compte POP3](locating-the-message-download-history-for-a-pop3-account.md) 
- [L'analyse de l'historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)    
- [Propriétés (API de gestion des comptes)](properties-account-management-api.md)
    

