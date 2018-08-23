---
title: Afficher les dossiers MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3a89588294f07dca97fb48e56d2cde890c3f80ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568818"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="265a4-103">Afficher les dossiers MAPI</span><span class="sxs-lookup"><span data-stu-id="265a4-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="265a4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="265a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="265a4-p101">Afficher les dossiers sont les dossiers racine qui contiennent des informations associ�es pour d�finir des mises en page de l'autre affichage pour le contenu des dossiers de message interpersonnel (IPM). Afficher les dossiers se trouvent sous la racine de la banque de messages et, par cons�quent, ne sont pas visibles dans l'application cliente classique. Non � chaque banque de messages inclut les dossiers d'affichage ; Seuls les banques de messages qui sont configur�s pour fonctionner en tant que la banque de messages par d�faut pour la session doivent inclure les.</span><span class="sxs-lookup"><span data-stu-id="265a4-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="265a4-108">MAPI prend en charge deux dossiers d'affichage :</span><span class="sxs-lookup"><span data-stu-id="265a4-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="265a4-109">Communes � Le dossier d'affichage communs contient des vues qui sont standard pour la banque de messages et peuvent �tre utilis�s par n'importe quel utilisateur d'un client qui acc�de � la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="265a4-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="265a4-110">L’identificateur d’entrée pour le dossier d’affichage communs est stocké dans la propriété **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) de la banque.</span><span class="sxs-lookup"><span data-stu-id="265a4-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="265a4-111">Personnel � Le dossier d'affichage personnel contient des vues qui sont d�finies par un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="265a4-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="265a4-112">MAPI définit la propriété **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) pour contenir l’identificateur d’entrée du dossier d’affichage personnel.</span><span class="sxs-lookup"><span data-stu-id="265a4-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="265a4-113">� l'aide des affichages personnels, par exemple, un utilisateur peut se pr�senter � un groupe de messages tri�s par exp�diteur, r�pertoriant uniquement l'objet et l'accus� de r�ception date du message ; un autre utilisateur pourrait ressembler au m�me groupe tri� par date, r�pertoriant le sujet, l'exp�diteur et la taille de message.</span><span class="sxs-lookup"><span data-stu-id="265a4-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="265a4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="265a4-114">See also</span></span>



[<span data-ttu-id="265a4-115">Dossiers MAPI</span><span class="sxs-lookup"><span data-stu-id="265a4-115">MAPI Folders</span></span>](mapi-folders.md)

