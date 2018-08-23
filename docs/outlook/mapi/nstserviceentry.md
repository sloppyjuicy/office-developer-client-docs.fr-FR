---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 85cfd219eb83592a4e01263caf5d6923db39e0cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583784"
---
# <a name="nstserviceentry"></a><span data-ttu-id="232dc-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="232dc-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="232dc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="232dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="232dc-105">Fonction de point d’entrée de service de message pour une MAPI stocker le fournisseur à utiliser un magasin local PST comme une banque NST.</span><span class="sxs-lookup"><span data-stu-id="232dc-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="232dc-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="232dc-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="232dc-107">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="232dc-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="232dc-108">Fournisseur MAPI</span><span class="sxs-lookup"><span data-stu-id="232dc-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="232dc-109">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="232dc-109">Called by:</span></span>  <br/> |<span data-ttu-id="232dc-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="232dc-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="232dc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="232dc-111">Parameters</span></span>

 <span data-ttu-id="232dc-112">**NSTServiceEntry** utilise le prototype de fonction **[MSGSERVICEENTRY](msgserviceentry.md)** .</span><span class="sxs-lookup"><span data-stu-id="232dc-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="232dc-113">Pour plus d’informations sur ses paramètres, voir **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="232dc-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="232dc-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="232dc-114">Return values</span></span>

<span data-ttu-id="232dc-115">Pour plus d’informations sur les valeurs de retour, voir **[MSGSERVICEENTRY](msgserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="232dc-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="232dc-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="232dc-116">Remarks</span></span>

<span data-ttu-id="232dc-117">Lorsque vous utilisez **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez « NSTServiceEntry » comme nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="232dc-117">When using **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="232dc-118">Pour utiliser l’API de réplication, un fournisseur de banque MAPI doit tout d’abord ouvrir et renvoyer un magasin local PST en appelant **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="232dc-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="232dc-119">Le fournisseur peut utiliser ensuite les interfaces principales des API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication.</span><span class="sxs-lookup"><span data-stu-id="232dc-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="232dc-120">Les notes suivantes s’appliquent à un magasin de NST :</span><span class="sxs-lookup"><span data-stu-id="232dc-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="232dc-121">Ne stockez pas les informations dans la section profil global lors de l’implémentation d’un fournisseur MAPI qui utilise **NSTServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="232dc-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="232dc-122">La section profil global est partagée par tous les fournisseurs et les données stockées dans ce profil peuvent être remplacées.</span><span class="sxs-lookup"><span data-stu-id="232dc-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="232dc-123">Uniquement les éléments dont les horodatages modification existant obtenir leurs cachets de mise à jour lorsqu’ils sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="232dc-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="232dc-124">Vérification des conflits ne produit pas automatiquement lorsque des éléments sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="232dc-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="232dc-125">Détection des doublons ne se produit pas lorsque des éléments sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="232dc-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="232dc-126">Le fichier représentant la version en cache du serveur est ajouté avec. NST.</span><span class="sxs-lookup"><span data-stu-id="232dc-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="232dc-127">Pour obtenir un pointeur vers la section profil global, un service de message appelle **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** dans l’objet de prise en charge à l’aide de **pbNSTGlobalProfileSectionGuid** tels que définis ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="232dc-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="232dc-128">Dans ce cas, l’objet de prise en charge du service de message doit garantir que **IMAPISupport::OpenProfileSection** retourne la section profil qui est identifiée par la propriété **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** dans la section de profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="232dc-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="232dc-129">Pour obtenir cette section de profil, l’objet de prise en charge peut ouvrir la section de profil par défaut, récupérez **PR_SERVICE_UID**et transmettre le résultat à **IMAPISupport::OpenProfileSection** pour récupérer la section profil global.</span><span class="sxs-lookup"><span data-stu-id="232dc-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="232dc-130">L’objet de prise en charge retourne à son tour un pointeur vers cette section de profil global pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="232dc-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="232dc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="232dc-131">See also</span></span>



[<span data-ttu-id="232dc-132">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="232dc-132">About the Replication API</span></span>](about-the-replication-api.md)

