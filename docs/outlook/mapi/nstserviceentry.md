---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280053"
---
# <a name="nstserviceentry"></a><span data-ttu-id="fa55d-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="fa55d-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="fa55d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa55d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa55d-105">Fonction de point d’entrée du service de messagerie pour qu’un fournisseur de magasin MAPI encapsule une boutique locale basée sur PST en tant que magasin NST.</span><span class="sxs-lookup"><span data-stu-id="fa55d-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fa55d-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fa55d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa55d-107">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="fa55d-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa55d-108">Fournisseur MAPI</span><span class="sxs-lookup"><span data-stu-id="fa55d-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="fa55d-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="fa55d-109">Called by:</span></span>  <br/> |<span data-ttu-id="fa55d-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa55d-110">MAPI</span></span>  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a><span data-ttu-id="fa55d-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="fa55d-111">Parameters</span></span>

 <span data-ttu-id="fa55d-112">**NSTServiceEntry utilise** le prototype de fonction **[MSGSERVICEENTRY.](msgserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="fa55d-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="fa55d-113">Pour plus d’informations sur ses paramètres, voir **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="fa55d-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="fa55d-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="fa55d-114">Return values</span></span>

<span data-ttu-id="fa55d-115">Pour plus d’informations sur les valeurs de retour, voir **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="fa55d-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa55d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa55d-116">Remarks</span></span>

<span data-ttu-id="fa55d-117">Lorsque vous **[utilisez GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez « NSTServiceEntry » comme nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="fa55d-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="fa55d-118">Pour utiliser l’API de réplication, un fournisseur de magasin MAPI doit d’abord ouvrir et encapsuler un magasin local basé sur PST en appelant **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="fa55d-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="fa55d-119">Le fournisseur peut ensuite utiliser les interfaces principales de l’API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication.</span><span class="sxs-lookup"><span data-stu-id="fa55d-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="fa55d-120">Les remarques suivantes s’appliquent à un magasin NST :</span><span class="sxs-lookup"><span data-stu-id="fa55d-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="fa55d-121">Ne stockez pas d’informations dans la section de profil global lors de l’implémentation d’un fournisseur MAPI qui utilise **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="fa55d-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="fa55d-122">La section profil global est partagée par de nombreux fournisseurs et les données stockées dans ce profil peuvent être écrasées.</span><span class="sxs-lookup"><span data-stu-id="fa55d-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="fa55d-123">Seuls les éléments avec des horodaages de modification existants obtiennent leurs cachets mis à jour lorsqu’ils sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fa55d-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="fa55d-124">La vérification des conflits ne se produit pas automatiquement lorsque des éléments sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fa55d-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="fa55d-125">La détection des doublons ne se produit pas lorsque des éléments sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fa55d-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="fa55d-126">Le fichier représentant la version mise en cache du serveur est fourni avec . NST.</span><span class="sxs-lookup"><span data-stu-id="fa55d-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="fa55d-127">Pour obtenir un pointeur vers la section profil global, un service de message appelle **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** dans l’objet de support à l’aide de **pbNSTGlobalProfileSectionGuid** comme défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="fa55d-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="fa55d-128">Dans ce cas, l’objet de support du service de message doit s’assurer que **IMAPISupport::OpenProfileSection** renvoie la section de profil identifiée par la propriété **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** dans la section de profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa55d-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="fa55d-129">Pour obtenir cette section de profil, l’objet de support peut ouvrir la section profil par défaut, récupérer **PR_SERVICE_UID** et transmettre le résultat à **IMAPISupport::OpenProfileSection** pour récupérer la section de profil global correcte.</span><span class="sxs-lookup"><span data-stu-id="fa55d-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="fa55d-130">L’objet de support renvoie à son tour un pointeur vers cette section de profil global vers le service de message.</span><span class="sxs-lookup"><span data-stu-id="fa55d-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fa55d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa55d-131">See also</span></span>



[<span data-ttu-id="fa55d-132">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="fa55d-132">About the Replication API</span></span>](about-the-replication-api.md)

