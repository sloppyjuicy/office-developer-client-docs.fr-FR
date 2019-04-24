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
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341600"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="ff2bf-103">Propriété canonique PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="ff2bf-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="ff2bf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff2bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff2bf-105">Spécifie la version complète et les informations de création relatives au serveur Microsoft Exchange auquel les comptes d'un profil sont connectés.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="ff2bf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ff2bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff2bf-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="ff2bf-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="ff2bf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ff2bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff2bf-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="ff2bf-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="ff2bf-110">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="ff2bf-110">Property type:</span></span>  <br/> |<span data-ttu-id="ff2bf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff2bf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff2bf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ff2bf-112">Area:</span></span>  <br/> |<span data-ttu-id="ff2bf-113">Configuration du profil MAPI</span><span class="sxs-lookup"><span data-stu-id="ff2bf-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff2bf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff2bf-114">Remarks</span></span>

<span data-ttu-id="ff2bf-115">Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="ff2bf-116">Les versions d'Outlook antérieures à Microsoft Office Outlook 2007 ne prennent pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="ff2bf-117">Pour ces versions d'Outlook, vérifiez l'existence de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** dans le profil.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="ff2bf-118">En règle générale, si la boîte aux lettres active est connectée à un serveur Exchange, Outlook 2007 stocke les informations de version d'Exchange Server dans la propriété **PR_PROFILE_SERVER_FULL_VERSION** du profil actif.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="ff2bf-119">Outlook stocke les informations dans une structure **EXCHANGE_STORE_VERSION_NUM** qui contient les numéros de version principale et secondaire, ainsi que les numéros de build principaux et secondaires.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="ff2bf-120">Par exemple, pour stocker l'identificateur de version d'Exchange Server **8.0.685.24**, le numéro de version majeure est 8 et le numéro de version mineure est 0 et le numéro de build majeur est 685 et le numéro de build mineur est 24.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="ff2bf-121">Seul un des **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d'exister dans un profil, mais il n'existe aucune garantie qui existe toujours dans un profil.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="ff2bf-122">Outlook ne peut pas écrire dans l'une ou l'autre des propriétés tant qu'il n'a pas réussi à se connecter au serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="ff2bf-123">Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l'objet **namespace** pour rechercher la version d'Exchange Server sur laquelle la boîte aux lettres active est hébergée.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff2bf-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="ff2bf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff2bf-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ff2bf-125">Protocol specifications</span></span>

<span data-ttu-id="ff2bf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff2bf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff2bf-127">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff2bf-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="ff2bf-128">Header files</span></span>

<span data-ttu-id="ff2bf-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ff2bf-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff2bf-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff2bf-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ff2bf-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ff2bf-132">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="ff2bf-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff2bf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff2bf-133">See also</span></span>



[<span data-ttu-id="ff2bf-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ff2bf-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff2bf-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ff2bf-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff2bf-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ff2bf-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff2bf-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ff2bf-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

