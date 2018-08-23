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
ms.openlocfilehash: 0712407a7882c449c065cb6816694b4a1611036f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568468"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="b8cba-103">Gestion d’une banque de messages</span><span class="sxs-lookup"><span data-stu-id="b8cba-103">Handling a message store</span></span>
  
<span data-ttu-id="b8cba-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8cba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8cba-105">Gestion d’une banque de messages est une part importante de l’ensemble d’un client de tâches.</span><span class="sxs-lookup"><span data-stu-id="b8cba-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="b8cba-106">Ces tâches incluent l’ouverture, copie, déplacement, l’ajout et suppression de dossiers et messages, affichage de tableaux de diverses, propriétés et contrôler les niveaux d’accès.</span><span class="sxs-lookup"><span data-stu-id="b8cba-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="b8cba-107">[L’ouverture d’une banque de messages](opening-a-message-store.md): explique comment ouvrir une ou plusieurs bases de messages pendant une session.</span><span class="sxs-lookup"><span data-stu-id="b8cba-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="b8cba-108">[Ouverture de la banque de messages par défaut](opening-the-default-message-store.md): décrit comment ouvrir la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8cba-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="b8cba-109">[Validation et l’initialisation d’une banque de messages](validating-and-initializing-a-message-store.md): explique comment initialiser et valider une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="b8cba-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="b8cba-110">[Recherche dans une banque de messages](searching-a-message-store.md): explique comment rechercher dans les dossiers d’un ou plusieurs de rechercher les messages qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="b8cba-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="b8cba-111">[Sélection d’un dossier de réception](selecting-a-receive-folder.md): décrit les étapes de création d’un dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="b8cba-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="b8cba-112">[L’ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md): explique comment ouvrir un dossier.</span><span class="sxs-lookup"><span data-stu-id="b8cba-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="b8cba-113">[Affichage d’une Table de contenu de dossier](displaying-a-folder-contents-table.md): décrit comment afficher le tableau contenu de dossier qui contient des informations récapitulatives sur tous ses messages.</span><span class="sxs-lookup"><span data-stu-id="b8cba-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="b8cba-114">[Parcourir le dossier boîte de réception](traversing-the-inbox-folder.md): décrit comment passer en revue tous les messages dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b8cba-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="b8cba-115">[Copie ou déplacement d’un Message ou un dossier](copying-or-moving-a-message-or-a-folder.md): explique comment copier ou déplacer un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="b8cba-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="b8cba-116">[Ouverture d’un Message](opening-a-message.md): décrit comment ouvrir un message.</span><span class="sxs-lookup"><span data-stu-id="b8cba-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="b8cba-117">[Recherche de l’icône d’un Message](finding-the-icon-for-a-message.md): explique comment trouver une icône qui est associée à un message.</span><span class="sxs-lookup"><span data-stu-id="b8cba-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="b8cba-118">[L’ouverture d’un descripteur d’affichage](opening-a-view-descriptor.md): décrit comment ouvrir un descripteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b8cba-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="b8cba-119">[Suppression d’un Message](deleting-a-message.md): explique comment supprimer un message.</span><span class="sxs-lookup"><span data-stu-id="b8cba-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="b8cba-120">[L’enregistrement d’un Message dans la boîte de réception](saving-a-message-in-the-inbox.md): décrit comment stocker un message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b8cba-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="b8cba-121">[Recherche envoyé ou enregistré les Messages](finding-sent-or-saved-messages.md): explique comment localiser tous les messages sortants qui ont été enregistrés ou envoyés.</span><span class="sxs-lookup"><span data-stu-id="b8cba-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="b8cba-122">[Suivi de Conversations](tracking-conversations.md): explique comment effectuer le suivi des conversations.</span><span class="sxs-lookup"><span data-stu-id="b8cba-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

