---
title: Récupération des propriétés d'un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328650"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="a1ee1-103">Récupération des propriétés d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="a1ee1-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="a1ee1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1ee1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1ee1-105">Pour émettre une requête significative pour un type de message personnalisé, une application doit déterminer les propriétés attendues sur ce message.</span><span class="sxs-lookup"><span data-stu-id="a1ee1-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="a1ee1-106">Pour obtenir la liste des propriétés utilisées par une classe de message personnalisée, une application cliente interroge le gestionnaire de formulaires MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1ee1-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="a1ee1-107">Le gestionnaire de formulaires obtient ces informations à partir du fichier de configuration de formulaire approprié afin que les applications clientes puissent utiliser ces informations sans avoir à activer le serveur de formulaire lui-même.</span><span class="sxs-lookup"><span data-stu-id="a1ee1-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="a1ee1-108">Pour ce faire, l'application cliente appelle la méthode [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) comme suit:</span><span class="sxs-lookup"><span data-stu-id="a1ee1-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="a1ee1-109">Notez que le troisième argument de **ResolveMessageClass** est le dossier qui contient la table des matières associée que la requête doit rechercher pour les serveurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="a1ee1-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="a1ee1-110">NULL indique que le gestionnaire de formulaire doit rechercher tous les conteneurs de formulaires disponibles.</span><span class="sxs-lookup"><span data-stu-id="a1ee1-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="a1ee1-111">Si la requête doit s'exécuter sur un dossier particulier, il est préférable d'inclure le pointeur [IMAPIFolder](imapifolderimapicontainer.md) approprié à la place.</span><span class="sxs-lookup"><span data-stu-id="a1ee1-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1ee1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1ee1-112">See also</span></span>



[<span data-ttu-id="a1ee1-113">Interactions de serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="a1ee1-113">Form Server Interactions</span></span>](form-server-interactions.md)

