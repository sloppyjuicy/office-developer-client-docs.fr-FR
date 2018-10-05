---
title: Propriété canonique PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400354"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="39551-103">Propriété canonique PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="39551-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="39551-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39551-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39551-105">Active l’authentification Kerberos d’une configuration de profil.</span><span class="sxs-lookup"><span data-stu-id="39551-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="39551-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="39551-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39551-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="39551-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="39551-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39551-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39551-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="39551-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="39551-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="39551-110">Data type:</span></span>  <br/> |<span data-ttu-id="39551-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39551-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="39551-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="39551-112">Area:</span></span>  <br/> |<span data-ttu-id="39551-113">Configuration d’un profil MAPI</span><span class="sxs-lookup"><span data-stu-id="39551-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39551-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="39551-114">Remarks</span></span>

<span data-ttu-id="39551-115">Définir cette propriété sur le nom de domaine du serveur d’annuaire de l’utilisateur permet à connexion directe pour le contrôleur de domaine (DC), qui est nécessaire pour un profil a été configuré pour utiliser l’authentification Kerberos par rapport à Microsoft Exchange Server 2007 et versions antérieures, en définissant **RPC_C_AUTHN_GSS_KERBEROS** dans **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="39551-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="39551-116">Microsoft Exchange Server 2010 et Exchange Server 2013 gérer les appels de carnet d’adresse apportées au serveur d’accès Client différent de celui dans lequel Exchange Server 2007 et versions antérieures les gérer.</span><span class="sxs-lookup"><span data-stu-id="39551-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="39551-117">Le processus DSProxy n’est plus utilisé, afin que l’authentification Kerberos peut s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="39551-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="39551-118">Toutefois, le client doit toujours communiquer avec le serveur Exchange, plutôt que directement avec le contrôleur de domaine ne peut pas être souhaitée : paramètre **PR_PROFILE_HOME_SERVER_FQDN** permet de l’éviter.</span><span class="sxs-lookup"><span data-stu-id="39551-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="39551-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="39551-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39551-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="39551-120">Protocol specifications</span></span>

<span data-ttu-id="39551-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39551-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39551-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="39551-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39551-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39551-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39551-124">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="39551-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39551-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="39551-125">Header files</span></span>

<span data-ttu-id="39551-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39551-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="39551-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="39551-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="39551-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="39551-128">Mapitags.h</span></span>
  
> <span data-ttu-id="39551-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="39551-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39551-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39551-130">See also</span></span>



[<span data-ttu-id="39551-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="39551-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39551-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="39551-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39551-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="39551-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39551-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="39551-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

