---
title: Propriété canonique PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786442"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="56556-103">Propriété canonique PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="56556-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="56556-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56556-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56556-105">Spécifie les informations de version et de compilation complètes sur le serveur Microsoft Exchange auxquels sont connectés les comptes dans un profil.</span><span class="sxs-lookup"><span data-stu-id="56556-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="56556-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="56556-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56556-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="56556-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="56556-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="56556-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56556-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="56556-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="56556-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="56556-110">Property type:</span></span>  <br/> |<span data-ttu-id="56556-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="56556-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="56556-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="56556-112">Area:</span></span>  <br/> |<span data-ttu-id="56556-113">Configuration d’un profil MAPI</span><span class="sxs-lookup"><span data-stu-id="56556-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56556-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="56556-114">Remarks</span></span>

<span data-ttu-id="56556-115">Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="56556-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="56556-116">Versions d’Outlook antérieures à Microsoft Office Outlook 2007 ne prennent pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="56556-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="56556-117">Pour les versions d’Outlook, vérifiez l’existence de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** dans le profil.</span><span class="sxs-lookup"><span data-stu-id="56556-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="56556-118">En règle générale, si la boîte aux lettres actif est connecté à un serveur Exchange, Outlook 2007 stocke des informations complètes sur la version Exchange Server dans la propriété **PR_PROFILE_SERVER_FULL_VERSION** dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="56556-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="56556-119">Outlook stocke les informations dans une structure **EXCHANGE_STORE_VERSION_NUM** qui contient les numéros de version principale et secondaire et les numéros de version principale et secondaire.</span><span class="sxs-lookup"><span data-stu-id="56556-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="56556-120">Par exemple, pour stocker l’identificateur de version d’Exchange Server de **8.0.685.24**, le numéro de version principale est 8 et numéro de version secondaire est 0 et le numéro de version majeur est 685 et numéro de version secondaire est 24.</span><span class="sxs-lookup"><span data-stu-id="56556-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="56556-121">Seul **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d’exister dans un profil, mais il n’existe aucune garantie que soit toujours existe dans un profil.</span><span class="sxs-lookup"><span data-stu-id="56556-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="56556-122">Outlook n’écrit pas dans des propriétés jusqu'à ce qu’il s’est connecté au serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="56556-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="56556-123">Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l’objet **NameSpace** pour trouver la version du serveur Exchange qui héberge la boîte aux lettres active.</span><span class="sxs-lookup"><span data-stu-id="56556-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56556-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="56556-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56556-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="56556-125">Protocol specifications</span></span>

<span data-ttu-id="56556-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56556-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56556-127">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="56556-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56556-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="56556-128">Header files</span></span>

<span data-ttu-id="56556-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56556-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="56556-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56556-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="56556-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="56556-131">Mapitags.h</span></span>
  
> <span data-ttu-id="56556-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="56556-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56556-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56556-133">See also</span></span>



[<span data-ttu-id="56556-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56556-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56556-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56556-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56556-136">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56556-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56556-137">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="56556-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

