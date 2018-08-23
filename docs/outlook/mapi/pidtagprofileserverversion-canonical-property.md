---
title: Propriété canonique PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 79b6461ca4a796b292b86f0f3bdbd8a39ad65863
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575678"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="bb0c4-103">Propriété canonique PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="bb0c4-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="bb0c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb0c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb0c4-105">Spécifie des informations sur la version de Microsoft Exchange Server à laquelle les comptes dans un profil Microsoft Outlook sont connectés.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="bb0c4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bb0c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb0c4-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="bb0c4-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="bb0c4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bb0c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb0c4-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="bb0c4-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="bb0c4-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="bb0c4-110">Property type:</span></span>  <br/> |<span data-ttu-id="bb0c4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bb0c4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bb0c4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bb0c4-112">Area:</span></span>  <br/> |<span data-ttu-id="bb0c4-113">Configuration d’un profil MAPI</span><span class="sxs-lookup"><span data-stu-id="bb0c4-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb0c4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb0c4-114">Remarks</span></span>

<span data-ttu-id="bb0c4-115">Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="bb0c4-116">Versions d’Outlook antérieures à Microsoft Office Outlook 2007 peuvent écrire dans cette propriété pour stocker les informations relatives à la version d’Exchange Server auquel le profil actif est connecté.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="bb0c4-117">Toutefois, le format des informations de version varie pour différentes versions d’Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="bb0c4-118">Par exemple, les banques Outlook dans **PR_PROFILE_SERVER_VERSION** la valeur décimale 6944 pour représenter uniquement la version principale numéro de build dans l’identificateur de version de **6.5.6944.3** pour Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="bb0c4-119">Pour une connexion à Exchange 2007, Outlook stocke le numéro de version principale et la version principale numéro de version dans une représentation hexadécimale concaténée de ces numéros dans la propriété.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="bb0c4-120">Un identificateur de version d’Exchange 2007 de **8.0.685.24** possède un numéro de version majeur 8 et un numéro de version majeur 685 en décimal.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="bb0c4-121">Conversion de deux nombres en hexadécimal, vous obtenez 0 x 8 et 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="bb0c4-122">Concaténation de ces deux nombres, Outlook stocke la valeur 0x82AD dans **PR_PROFILE_SERVER_VERSION** en représentation hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="bb0c4-123">Outlook 2007 ne pas lire ou écrire cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="bb0c4-124">Il prend en charge **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="bb0c4-125">Seul **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d’exister dans un profil, mais il n’existe aucune garantie que soit toujours existe dans un profil.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="bb0c4-126">Outlook n’écrit pas dans des propriétés jusqu'à ce qu’il s’est connecté au serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="bb0c4-127">Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l’objet **NameSpace** pour trouver la version du serveur Exchange qui héberge la boîte aux lettres active.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb0c4-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bb0c4-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb0c4-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bb0c4-129">Protocol specifications</span></span>

<span data-ttu-id="bb0c4-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb0c4-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb0c4-131">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb0c4-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bb0c4-132">Header files</span></span>

<span data-ttu-id="bb0c4-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb0c4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb0c4-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb0c4-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="bb0c4-135">Mapitags.h</span></span>
  
> <span data-ttu-id="bb0c4-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="bb0c4-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb0c4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb0c4-137">See also</span></span>



[<span data-ttu-id="bb0c4-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bb0c4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb0c4-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bb0c4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb0c4-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bb0c4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb0c4-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bb0c4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

