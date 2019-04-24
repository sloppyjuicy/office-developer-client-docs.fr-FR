---
title: Gestion d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299481"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="8a2aa-103">Gestion d’une banque de messages</span><span class="sxs-lookup"><span data-stu-id="8a2aa-103">Handling a message store</span></span>
  
<span data-ttu-id="8a2aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a2aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a2aa-105">La gestion d'une banque de messages est une partie importante de l'ensemble des tâches d'un client.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="8a2aa-106">Ces tâches incluent l'ouverture, la copie, le mouvement, l'ajout et la suppression de dossiers et de messages, l'affichage de différentes tables, la définition de propriétés et le contrôle des niveaux d'accès.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="8a2aa-107">[Ouverture d'une banque de messages](opening-a-message-store.md): décrit comment ouvrir un ou plusieurs magasins de messages au cours d'une session.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="8a2aa-108">[Ouverture de la Banque de messages par défaut](opening-the-default-message-store.md): décrit l'ouverture de la Banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="8a2aa-109">[Validation et initialisation d'une banque de messages](validating-and-initializing-a-message-store.md): décrit la procédure d'initialisation et de validation d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="8a2aa-110">[Recherche dans une banque de messages](searching-a-message-store.md): décrit comment rechercher un ou plusieurs dossiers à la recherche de messages qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="8a2aa-111">[Sélection d'un dossier de réception](selecting-a-receive-folder.md): décrit les étapes de création d'un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="8a2aa-112">[Ouverture d'un dossier de banque de messages](opening-a-message-store-folder.md): décrit comment ouvrir un dossier.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="8a2aa-113">[Affichage d'une table de contenu de dossier](displaying-a-folder-contents-table.md): décrit comment afficher la table de contenu de dossier qui contient des informations récapitulatives sur tous ses messages.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="8a2aa-114">[Parcourir le dossier boîte de réception](traversing-the-inbox-folder.md): décrit comment parcourir tous les messages dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="8a2aa-115">[Copie ou déplacement d'un message ou d'un dossier](copying-or-moving-a-message-or-a-folder.md): décrit comment copier ou déplacer un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="8a2aa-116">[Ouverture d'un message](opening-a-message.md): décrit comment ouvrir un message.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="8a2aa-117">[Recherche de l'icône d'un message](finding-the-icon-for-a-message.md): décrit comment rechercher une icône associée à un message.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="8a2aa-118">[Ouverture d'un](opening-a-view-descriptor.md)descriptEur d'affichage: décrit comment ouvrir un descripteur de vue.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="8a2aa-119">[Suppression d'un message](deleting-a-message.md): décrit comment supprimer un message.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="8a2aa-120">[Enregistrement d'un message dans la boîte de réception](saving-a-message-in-the-inbox.md): décrit comment stocker un message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="8a2aa-121">[Recherche de messages envoyés ou enregistrés](finding-sent-or-saved-messages.md): explique comment localiser tous les messages sortants qui ont été enregistrés ou envoyés.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="8a2aa-122">[Suivi des conversations](tracking-conversations.md): décrit comment suivre les conversations.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

