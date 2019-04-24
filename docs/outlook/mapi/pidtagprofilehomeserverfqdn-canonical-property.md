---
title: Propriété canonique PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341593"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="87c19-103">Propriété canonique PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="87c19-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="87c19-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87c19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87c19-105">Active l'authentification Kerberos d'une configuration de profil.</span><span class="sxs-lookup"><span data-stu-id="87c19-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="87c19-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="87c19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87c19-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="87c19-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="87c19-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="87c19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87c19-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="87c19-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="87c19-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="87c19-110">Data type:</span></span>  <br/> |<span data-ttu-id="87c19-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87c19-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="87c19-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="87c19-112">Area:</span></span>  <br/> |<span data-ttu-id="87c19-113">Configuration du profil MAPI</span><span class="sxs-lookup"><span data-stu-id="87c19-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87c19-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="87c19-114">Remarks</span></span>

<span data-ttu-id="87c19-115">La définition de cette propriété sur le nom de domaine du serveur d'annuaire de l'utilisateur autorise une connexion directe au contrôleur de domaine (DC), nécessaire pour un profil qui a été configuré pour utiliser l'authentification Kerberos avec Microsoft Exchange Server 2007 et versions antérieures, en définissant **RPC_C_AUTHN_GSS_KERBEROS** dans **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="87c19-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="87c19-116">Microsoft Exchange Server 2010 et Exchange Server 2013 gèrent les appels de carnet d'adresses effectués sur le serveur d'accès au client différemment de la façon dont Exchange Server 2007 et les versions antérieures les gèrent.</span><span class="sxs-lookup"><span data-stu-id="87c19-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="87c19-117">Le processus DSProxy n'est plus utilisé, de sorte que l'authentification Kerberos peut réussir.</span><span class="sxs-lookup"><span data-stu-id="87c19-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="87c19-118">Toutefois, le client communique toujours avec le serveur Exchange au lieu d'être directement avec le contrôleur de contexte, ce qui n'est peut-être pas souhaité: la définition de **PR_PROFILE_HOME_SERVER_FQDN** évite cela.</span><span class="sxs-lookup"><span data-stu-id="87c19-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="87c19-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="87c19-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87c19-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="87c19-120">Protocol specifications</span></span>

<span data-ttu-id="87c19-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87c19-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87c19-122">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="87c19-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87c19-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87c19-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87c19-124">Spécifie les opérations admissibles pour les objets principaux de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="87c19-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87c19-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="87c19-125">Header files</span></span>

<span data-ttu-id="87c19-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87c19-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="87c19-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="87c19-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="87c19-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="87c19-128">Mapitags.h</span></span>
  
> <span data-ttu-id="87c19-129">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="87c19-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87c19-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c19-130">See also</span></span>



[<span data-ttu-id="87c19-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="87c19-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87c19-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="87c19-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87c19-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="87c19-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87c19-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="87c19-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

