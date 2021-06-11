---
title: Gestion d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407542"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="26f6e-103">Gestion d’une banque de messages</span><span class="sxs-lookup"><span data-stu-id="26f6e-103">Handling a message store</span></span>
  
<span data-ttu-id="26f6e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26f6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26f6e-105">La gestion d’une magasin de messages est une partie importante de l’ensemble de tâches de tout client.</span><span class="sxs-lookup"><span data-stu-id="26f6e-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="26f6e-106">Ces tâches incluent l’ouverture, la copie, le déplacement, l’ajout et la suppression de dossiers et de messages, l’affichage de différents tableaux, la définition de propriétés et le contrôle des niveaux d’accès.</span><span class="sxs-lookup"><span data-stu-id="26f6e-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="26f6e-107">[Ouverture d’une magasin de](opening-a-message-store.md)messages : décrit comment ouvrir une ou plusieurs magasins de messages au cours d’une session.</span><span class="sxs-lookup"><span data-stu-id="26f6e-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="26f6e-108">[Ouverture de la magasin de messages par défaut](opening-the-default-message-store.md): décrit comment ouvrir la magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="26f6e-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="26f6e-109">[Validation et initialisation d’une magasin de](validating-and-initializing-a-message-store.md)messages : décrit comment initialiser et valider une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="26f6e-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="26f6e-110">[Recherche dans une magasin de messages](searching-a-message-store.md): décrit comment rechercher des messages qui correspondent aux critères de recherche dans un ou plusieurs dossiers.</span><span class="sxs-lookup"><span data-stu-id="26f6e-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="26f6e-111">[Sélection d’un dossier de réception](selecting-a-receive-folder.md): décrit les étapes de création d’un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="26f6e-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="26f6e-112">[Ouverture d’un dossier de la boutique de messages](opening-a-message-store-folder.md): décrit comment ouvrir un dossier.</span><span class="sxs-lookup"><span data-stu-id="26f6e-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="26f6e-113">[Affichage d’une table des matières des](displaying-a-folder-contents-table.md)dossiers : décrit comment afficher la table des matières du dossier qui contient des informations récapitulatifs sur tous ses messages.</span><span class="sxs-lookup"><span data-stu-id="26f6e-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="26f6e-114">[Traversée du dossier Boîte de réception](traversing-the-inbox-folder.md): décrit comment parcourir tous les messages de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="26f6e-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="26f6e-115">[Copie ou déplacement d’un message ou](copying-or-moving-a-message-or-a-folder.md)d’un dossier : décrit comment copier ou déplacer un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="26f6e-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="26f6e-116">[Ouverture d’un message](opening-a-message.md): décrit comment ouvrir un message.</span><span class="sxs-lookup"><span data-stu-id="26f6e-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="26f6e-117">[Recherche de l’icône d’un message](finding-the-icon-for-a-message.md): décrit comment trouver une icône associée à un message.</span><span class="sxs-lookup"><span data-stu-id="26f6e-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="26f6e-118">[Ouverture d’un descripteur d’affichage](opening-a-view-descriptor.md): décrit comment ouvrir un descripteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="26f6e-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="26f6e-119">[Suppression d’un message](deleting-a-message.md): décrit comment supprimer un message.</span><span class="sxs-lookup"><span data-stu-id="26f6e-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="26f6e-120">[Enregistrement d’un message dans la](saving-a-message-in-the-inbox.md)boîte de réception : décrit comment stocker un message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="26f6e-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="26f6e-121">[Recherche des messages envoyés](finding-sent-or-saved-messages.md)ou enregistrés : décrit comment localiser tous les messages sortants qui ont été enregistrés ou envoyés.</span><span class="sxs-lookup"><span data-stu-id="26f6e-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="26f6e-122">[Suivi des conversations](tracking-conversations.md): décrit comment suivre les conversations.</span><span class="sxs-lookup"><span data-stu-id="26f6e-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

