---
title: Enregistrement des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425889"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="3972d-103">Enregistrement des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3972d-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="3972d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3972d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3972d-105">De nombreux objets prennent en charge un modèle de transaction de traitement dans lequel les modifications apportées aux propriétés ne sont pas permanentes tant qu'elles n'ont pas été validées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3972d-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="3972d-106">Tandis que les modifications apportées aux propriétés sont gérées par les méthodes [IMAPIProp:: SetProps](imapiprop-setprops.md) et [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) , l'étape de validation est gérée par [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="3972d-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="3972d-107">Il n'est pas possible d'accéder à la version la plus récente des propriétés d'un objet après un appel réussi à **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="3972d-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="3972d-108">Lorsque **SaveChanges** renvoie la valeur d'erreur MAPI_E_OBJECT_CHANGED, il s'agit d'un avertissement indiquant qu'un autre client valide simultanément les modifications apportées à l'objet.</span><span class="sxs-lookup"><span data-stu-id="3972d-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="3972d-109">Selon le fournisseur qui implémente l'objet, il est possible que plusieurs clients ouvrent correctement un objet en appelant sa méthode **OpenEntry** avec l'indicateur MAPI_MODIFY défini, en leur donnant accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3972d-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="3972d-110">L'objet renvoyé par un appel **OpenEntry** est une capture instantanée des données de stockage.</span><span class="sxs-lookup"><span data-stu-id="3972d-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="3972d-111">Chaque tentative ultérieure de modification de ces données peut remplacer la tentative précédente.</span><span class="sxs-lookup"><span data-stu-id="3972d-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="3972d-112">Lors de la réception de MAPI_E_OBJECT_CHANGED à partir d' **SaveChanges**, un client a la possibilité de:</span><span class="sxs-lookup"><span data-stu-id="3972d-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="3972d-113">Effectuez une copie de l'objet pour conserver les modifications.</span><span class="sxs-lookup"><span data-stu-id="3972d-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="3972d-114">Appeler **SaveChanges**en spécifiant FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="3972d-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="3972d-115">L'appel de **SaveChanges** avec l'indicateur FORCE_SAVE remplace l'enregistrement précédent et rend les modifications d'un client permanentes.</span><span class="sxs-lookup"><span data-stu-id="3972d-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3972d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3972d-116">See also</span></span>



[<span data-ttu-id="3972d-117">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="3972d-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

