---
title: À propos de la dernière heure de mise à jour d'un carnet d'adresses en mode hors connexion
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: Un hors connexion carnet d'adresses (OAB) permet aux utilisateurs de Outlook dans un état déconnecté l'accès aux informations d'annuaire à partir de la liste d'adresses globale (LAG) et d'autres carnets d'adresses.
ms.openlocfilehash: b1e3ff012606615e5e962c400f86ab5ee2fbed83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782564"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a><span data-ttu-id="dbe08-103">À propos de la dernière heure de mise à jour d'un carnet d'adresses en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="dbe08-103">About the last update time of an Offline Address Book</span></span>

<span data-ttu-id="dbe08-p101">Un hors connexion carnet d'adresses (OAB) permet aux utilisateurs de Outlook dans un état déconnecté l'accès aux informations d'annuaire à partir de la liste d'adresses globale (LAG) et d'autres carnets d'adresses. Il s'agit d'une copie d'un carnet d'adresses Outlook a téléchargé à partir d'un serveur Exchange pour fournir un accès en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dbe08-p101">An Offline Address Book (OAB) provides Outlook users in a disconnected state access to directory information from the Global Address List (GAL) and from other address books. It is a copy of an Address Book that Outlook has downloaded from an Exchange server to provide offline access.</span></span>
  
<span data-ttu-id="dbe08-p102">Les administrateurs Exchange peuvent choisir les carnets d'adresses pour le rendre disponible pour les utilisateurs qui travaillent en mode hors connexion. Pour créer une copie d'un carnet d'adresses, Exchange génère des nouveaux fichiers de carnet d'adresses, compresse les fichiers et les place dans un partage local. Selon la configuration de Outlook, Outlook télécharge les fichiers de carnet d'adresses à partir du Web ou d'un dossier Public sur un ordinateur client pour utiliser dans un état déconnecté. Outlook vérifie périodiquement et télécharge les mises à jour du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="dbe08-p102">Exchange administrators can choose which Address Books to make available for users who work offline. To create a copy of an Address Book, Exchange generates new OAB files, compresses the files, and places them on a local share. Depending on how Outlook is configured, Outlook downloads the OAB files either from the Web or from a Public Folder to a client computer for use in a disconnected state. Outlook periodically checks for and downloads OAB updates.</span></span>
  
<span data-ttu-id="dbe08-p103">Vous devrez permettant de savoir quand le carnet d'adresses a été mis à jour à partir du serveur Exchange de solutions Outlook que vous souhaitez fournir aux utilisateurs l'accès à un carnet d'adresses en mode hors connexion. Pour trouver la dernière heure de mise à jour d'un carnet d'adresses, les solutions peuvent utiliser l'entrée suivante dans le Registre Windows : **Heure de dernière modification HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB**. Le type de cette entrée de Registre est **REG_BINARY**. Les données sont la taille de 8 octets. Vous pouvez convertir les données vers une structure [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) de 64 bits spécification d'une valeur de temps universel coordonné (UTC) que Outlook téléchargé dernière les fichiers de carnet d'adresses à partir du serveur Exchange sur l'ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="dbe08-p103">Outlook solutions that want to provide their users offline access to an OAB may need to find out when the OAB was last updated from the Exchange server. To find the last update time of an OAB, solutions can use the following entry in the Windows registry: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB Last Modified Time**. The type of this registry entry is **REG_BINARY**. The data is 8 bytes in size. You can convert the data to a 64-bit [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) structure specifying a Universal Coordinated Time (UTC) value that Outlook last downloaded the OAB files from the Exchange server to the client computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbe08-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe08-115">See also</span></span>

- [<span data-ttu-id="dbe08-116">Managing Offline Address Books</span><span class="sxs-lookup"><span data-stu-id="dbe08-116">Managing Offline Address Books</span></span>](http://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

