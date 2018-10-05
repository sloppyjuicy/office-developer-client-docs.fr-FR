---
title: À propos de la dernière heure de mise à jour d'un carnet d'adresses en mode hors connexion
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: Un hors connexion carnet d'adresses (OAB) permet aux utilisateurs de Outlook dans un état déconnecté l'accès aux informations d'annuaire à partir de la liste d'adresses globale (LAG) et d'autres carnets d'adresses.
ms.openlocfilehash: 3374f87cd62d46a80ed823bff0516115a58c155c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392283"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a>À propos de la dernière heure de mise à jour d'un carnet d'adresses en mode hors connexion

Un hors connexion carnet d'adresses (OAB) permet aux utilisateurs de Outlook dans un état déconnecté l'accès aux informations d'annuaire à partir de la liste d'adresses globale (LAG) et d'autres carnets d'adresses. Il s'agit d'une copie d'un carnet d'adresses Outlook a téléchargé à partir d'un serveur Exchange pour fournir un accès en mode hors connexion.
  
Les administrateurs Exchange peuvent choisir les carnets d'adresses pour le rendre disponible pour les utilisateurs qui travaillent en mode hors connexion. Pour créer une copie d'un carnet d'adresses, Exchange génère des nouveaux fichiers de carnet d'adresses, compresse les fichiers et les place dans un partage local. Selon la configuration de Outlook, Outlook télécharge les fichiers de carnet d'adresses à partir du Web ou d'un dossier Public sur un ordinateur client pour utiliser dans un état déconnecté. Outlook vérifie périodiquement et télécharge les mises à jour du carnet d'adresses.
  
Vous devrez permettant de savoir quand le carnet d'adresses a été mis à jour à partir du serveur Exchange de solutions Outlook que vous souhaitez fournir aux utilisateurs l'accès à un carnet d'adresses en mode hors connexion. Pour trouver la dernière heure de mise à jour d'un carnet d'adresses, les solutions peuvent utiliser l'entrée suivante dans le Registre Windows : **Heure de dernière modification HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB**. Le type de cette entrée de Registre est **REG_BINARY**. Les données sont la taille de 8 octets. Vous pouvez convertir les données vers une structure [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) de 64 bits spécification d'une valeur de temps universel coordonné (UTC) que Outlook téléchargé dernière les fichiers de carnet d'adresses à partir du serveur Exchange sur l'ordinateur client. 
  
## <a name="see-also"></a>Voir aussi

- [Managing Offline Address Books](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

