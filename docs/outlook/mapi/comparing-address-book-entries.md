---
title: Comparaison des entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415354"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="5d7be-103">Comparaison des entrées de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="5d7be-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="5d7be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d7be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d7be-105">L’implémentation [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) de votre fournisseur compare les identificateurs d’entrée pour deux des objets de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d7be-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="5d7be-106">MAPI appelle cette méthode après avoir déterminé que les deux identificateurs d’entrée contiennent le [MAPIUID](mapiuid.md)enregistré de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d7be-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="5d7be-107">Par conséquent, votre méthode **CompareEntryIDs n’a** pas besoin de vérifier que les identificateurs d’entrée transmis pour les paramètres  _lpEntryID1_ et  _lpEntryID2_ appartiennent à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d7be-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="5d7be-108">Appeler **IABLogon::CompareEntryIDs** équivaut à récupérer la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour chacun des deux objets et à les comparer directement.</span><span class="sxs-lookup"><span data-stu-id="5d7be-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="5d7be-109">**Pour implémenter CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="5d7be-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="5d7be-110">Vérifiez le type des identificateurs d’entrée transmis si votre fournisseur stocke ces informations.</span><span class="sxs-lookup"><span data-stu-id="5d7be-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="5d7be-111">Par exemple, un identificateur d’entrée peut appartenir à un utilisateur de messagerie, tandis que l’autre peut appartenir à une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="5d7be-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="5d7be-112">Si les types ne correspondent pas, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyez.</span><span class="sxs-lookup"><span data-stu-id="5d7be-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="5d7be-113">Comparez les tailles des deux identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5d7be-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="5d7be-114">S’ils ne sont pas identiques, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="5d7be-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="5d7be-115">Vérifiez que la taille des identificateurs d’entrée est la taille correcte pour leur type.</span><span class="sxs-lookup"><span data-stu-id="5d7be-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="5d7be-116">Si ce n’est pas le cas, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyez la valeur d’erreur MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="5d7be-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="5d7be-117">Vérifiez si les identificateurs d’entrée sont identiques.</span><span class="sxs-lookup"><span data-stu-id="5d7be-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="5d7be-118">S’ils sont comparés de manière égale, définissez le contenu du paramètre  _lpulResult_ sur TRUE et renvoyer.</span><span class="sxs-lookup"><span data-stu-id="5d7be-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="5d7be-119">Sinon, définissez-la sur FALSE avant de la renvoyer.</span><span class="sxs-lookup"><span data-stu-id="5d7be-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="5d7be-120">Si votre fournisseur compare un identificateur d’entrée à court terme à un identificateur à long terme, il doit comparer de la même manière.</span><span class="sxs-lookup"><span data-stu-id="5d7be-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

