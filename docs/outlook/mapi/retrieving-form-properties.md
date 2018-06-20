---
title: Récupération des propriétés de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787024"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="907c0-103">Récupération des propriétés de formulaire</span><span class="sxs-lookup"><span data-stu-id="907c0-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="907c0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="907c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="907c0-105">Pour émettre une requête qui est explicite à un type de message personnalisé, une application a besoin de connaître les propriétés attendu sur ce message.</span><span class="sxs-lookup"><span data-stu-id="907c0-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="907c0-106">Pour obtenir une liste des propriétés qui utilise une classe de message personnalisée, une application cliente interroge le Gestionnaire de formulaire MAPI.</span><span class="sxs-lookup"><span data-stu-id="907c0-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="907c0-107">Le Gestionnaire de formulaire obtient ces informations à partir du fichier de configuration de formulaire adéquat afin que les applications clientes peuvent utiliser ces informations sans la surcharge d’activation du serveur du formulaire lui-même.</span><span class="sxs-lookup"><span data-stu-id="907c0-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="907c0-108">Pour ce faire, l’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) comme suit :</span><span class="sxs-lookup"><span data-stu-id="907c0-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="907c0-109">Notez que le troisième argument de **ResolveMessageClass** est le dossier qui contient la table de contenu associé à la requête de recherche pour les serveurs du formulaire.</span><span class="sxs-lookup"><span data-stu-id="907c0-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="907c0-110">NULL indique que le Gestionnaire de formulaire doit rechercher tous les conteneurs de formulaires disponibles.</span><span class="sxs-lookup"><span data-stu-id="907c0-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="907c0-111">Si la requête doit s’exécuter par rapport à un dossier particulier, il est préférable d’inclure le pointeur [IMAPIFolder](imapifolderimapicontainer.md) approprié à la place.</span><span class="sxs-lookup"><span data-stu-id="907c0-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="907c0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="907c0-112">See also</span></span>



[<span data-ttu-id="907c0-113">Formulaire serveur Interactions</span><span class="sxs-lookup"><span data-stu-id="907c0-113">Form Server Interactions</span></span>](form-server-interactions.md)

