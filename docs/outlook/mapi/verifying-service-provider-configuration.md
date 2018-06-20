---
title: Vérification de la configuration de fournisseur de service
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 047a3b99b2d615984252071a1264521a4b2240f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787461"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="3e7f3-103">Vérification de la configuration de fournisseur de service</span><span class="sxs-lookup"><span data-stu-id="3e7f3-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="3e7f3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e7f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e7f3-105">Votre méthode d’ouverture de session ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) doit vérifier la configuration de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="3e7f3-106">Cela consiste à vérifier que toutes les propriétés nécessaires pour l’opération complète sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="3e7f3-107">Chaque fournisseur nécessite un nombre différent de propriétés. configuration dépend de votre fournisseur et le degré d’interaction utilisateur que vous autorisez.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="3e7f3-108">Certains fournisseurs de services conserver toutes les propriétés nécessaires dans le profil.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="3e7f3-109">Autres fournisseurs de services de conserver un jeu de propriétés partiel dans le profil et invite l’utilisateur pour les valeurs manquantes.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="3e7f3-110">Toujours autres fournisseurs ne stockent pas les propriétés dans le profil, tout dépend de l’utilisateur à fournir toutes les informations nécessaires pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="3e7f3-111">Pour récupérer les propriétés stockées dans le profil</span><span class="sxs-lookup"><span data-stu-id="3e7f3-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="3e7f3-112">Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), en passant le [MAPIUID](mapiuid.md) de votre fournisseur comme un paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="3e7f3-113">Appeler des méthodes de la section profil [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) pour récupérer les propriétés individuelles ou une liste de propriétés.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="3e7f3-114">Pour définir les propriétés à partir des informations utilisateur</span><span class="sxs-lookup"><span data-stu-id="3e7f3-114">To set properties from user information</span></span>
  
<span data-ttu-id="3e7f3-115">Afficher une feuille de propriétés, si MAPI n’a pas défini un indicateur interdisant l’affichage.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="3e7f3-116">Les indicateurs suivants indiquent qu’une interface utilisateur ne peut pas être présentée.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="3e7f3-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="3e7f3-117">**Flag**</span></span>|<span data-ttu-id="3e7f3-118">**Fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="3e7f3-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e7f3-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="3e7f3-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="3e7f3-120">Fournisseur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="3e7f3-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="3e7f3-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="3e7f3-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="3e7f3-122">Fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="3e7f3-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="3e7f3-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="3e7f3-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="3e7f3-124">Fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="3e7f3-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="3e7f3-125">Si votre fournisseur ne stocke pas toutes ses propriétés de configuration dans le profil, solliciter l’utilisateur et MAPI un des indicateurs de suppression boîte dialogue passe à votre méthode d’ouverture de session, retourne MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="3e7f3-126">Renvoie également cette erreur lors de l’indicateur de suppression de boîte de dialogue n’est pas défini, mais l’utilisateur ne fournit pas toutes les informations requises.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="3e7f3-127">En cas de votre fournisseur de services de la méthode d’ouverture de session avec MAPI_E_UNCONFIGURED, MAPI appelle de nouveau la fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="3e7f3-128">Si les informations ne peut pas être localisées avec le deuxième appel, la session peut arrêter, selon l’importance de votre fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="3e7f3-129">L’illustration suivante montre la logique requise pour la configuration de votre méthode d’ouverture de session service fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3e7f3-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="3e7f3-130">**Organigramme de vérification de configuration**</span><span class="sxs-lookup"><span data-stu-id="3e7f3-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="3e7f3-131">![Organigramme de vérification de configuration] (media/amapi_62.gif "Organigramme de vérification de configuration")</span><span class="sxs-lookup"><span data-stu-id="3e7f3-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e7f3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e7f3-132">See also</span></span>

- [<span data-ttu-id="3e7f3-133">L’implémentation du fournisseur de Service d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="3e7f3-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

