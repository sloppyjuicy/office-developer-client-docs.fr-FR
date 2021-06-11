---
title: Vérification de la configuration du fournisseur de services
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418847"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="254e9-103">Vérification de la configuration du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="254e9-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="254e9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="254e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="254e9-105">Votre méthode d’logon ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) doit vérifier la configuration de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="254e9-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="254e9-106">Cela implique de vérifier que toutes les propriétés requises pour un fonctionnement complet sont définies correctement.</span><span class="sxs-lookup"><span data-stu-id="254e9-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="254e9-107">Chaque fournisseur nécessite un nombre différent de propriétés ; dépend de votre fournisseur et du degré d’interaction utilisateur que vous autorisez.</span><span class="sxs-lookup"><span data-stu-id="254e9-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="254e9-108">Certains fournisseurs de services conservent toutes les propriétés nécessaires dans le profil.</span><span class="sxs-lookup"><span data-stu-id="254e9-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="254e9-109">D’autres fournisseurs de services conservent un ensemble partiel de propriétés dans le profil et invitent l’utilisateur à lui faire part de l’absence de valeurs.</span><span class="sxs-lookup"><span data-stu-id="254e9-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="254e9-110">D’autres fournisseurs ne stockent pas du tout les propriétés dans le profil, en s’appuyant sur l’utilisateur pour fournir toutes les informations nécessaires à la configuration.</span><span class="sxs-lookup"><span data-stu-id="254e9-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="254e9-111">Pour récupérer les propriétés stockées dans le profil</span><span class="sxs-lookup"><span data-stu-id="254e9-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="254e9-112">Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), en passant le [MAPIUID](mapiuid.md) de votre fournisseur comme paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="254e9-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="254e9-113">Appelez les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la section de profil pour récupérer des propriétés individuelles ou une liste de propriétés.</span><span class="sxs-lookup"><span data-stu-id="254e9-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="254e9-114">Pour définir des propriétés à partir des informations utilisateur</span><span class="sxs-lookup"><span data-stu-id="254e9-114">To set properties from user information</span></span>
  
<span data-ttu-id="254e9-115">Afficher une feuille de propriétés, si MAPI n’a pas définie d’indicateur qui interdit l’affichage.</span><span class="sxs-lookup"><span data-stu-id="254e9-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="254e9-116">Les indicateurs suivants indiquent qu’une interface utilisateur ne peut pas être présentée.</span><span class="sxs-lookup"><span data-stu-id="254e9-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="254e9-117">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="254e9-117">**Flag**</span></span>|<span data-ttu-id="254e9-118">**Fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="254e9-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="254e9-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="254e9-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="254e9-120">Fournisseur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="254e9-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="254e9-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="254e9-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="254e9-122">Fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="254e9-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="254e9-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="254e9-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="254e9-124">Fournisseur de magasin de messages</span><span class="sxs-lookup"><span data-stu-id="254e9-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="254e9-125">Si votre fournisseur ne stocke pas toutes ses propriétés de configuration dans le profil, ce qui nécessite une interaction de l’utilisateur et que MAPI transmet l’un des indicateurs de suppression de la boîte de dialogue à votre méthode d’ouverture de MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="254e9-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="254e9-126">Renvoyer également cette erreur lorsque l’indicateur de suppression de boîte de dialogue n’est pas définie, mais que l’utilisateur ne fournit pas toutes les informations requises.</span><span class="sxs-lookup"><span data-stu-id="254e9-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="254e9-127">Lorsque votre fournisseur de services échoue à sa méthode d’MAPI_E_UNCONFIGURED, MAPI appelle à nouveau votre fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="254e9-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="254e9-128">Si les informations ne peuvent pas être localisées avec le deuxième appel, la session peut s’interrompre, selon l’importance de votre fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="254e9-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="254e9-129">L’illustration suivante illustre la logique requise pour la configuration dans votre méthode d’accès au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="254e9-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="254e9-130">**Diagramme de flux de vérification de la configuration**</span><span class="sxs-lookup"><span data-stu-id="254e9-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="254e9-131">![Flowchart de vérification de l’écran de]configuration de la vérification(media/amapi_62.gif "de la configuration")</span><span class="sxs-lookup"><span data-stu-id="254e9-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="254e9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="254e9-132">See also</span></span>

- [<span data-ttu-id="254e9-133">Mise en œuvre de l’logo du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="254e9-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

