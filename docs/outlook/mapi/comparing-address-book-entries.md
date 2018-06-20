---
title: Comparaison des entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783043"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="45c49-103">Comparaison des entrées de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="45c49-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="45c49-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45c49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45c49-105">Implémentation de votre fournisseur [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) compare les identificateurs d’entrée de deux des objets de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="45c49-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="45c49-106">MAPI appelle cette méthode après que détermination que les identificateurs de deux entrée contenant votre fournisseur inscrit [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="45c49-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="45c49-107">Par conséquent, votre méthode **CompareEntryIDs** doit vérifier pas que les identificateurs d’entrée passés pour les paramètres _lpEntryID1_ et _lpEntryID2_ appartiennent à votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="45c49-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="45c49-108">**IABLogon::CompareEntryIDs** équivaut à la récupération de la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour chacun des deux objets et en les comparant directement.</span><span class="sxs-lookup"><span data-stu-id="45c49-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="45c49-109">**Pour implémenter CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="45c49-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="45c49-110">Vérifier le type des identificateurs d’entrée passé si votre fournisseur enregistre ces informations.</span><span class="sxs-lookup"><span data-stu-id="45c49-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="45c49-111">Par exemple, un identificateur d’entrée peut appartenir à un utilisateur de messagerie pendant que l’autre peut appartenir à une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="45c49-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="45c49-112">Si les types ne correspondent pas, le contenu du paramètre _lpulResult_ la valeur FALSE et retour.</span><span class="sxs-lookup"><span data-stu-id="45c49-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="45c49-113">Comparer les tailles des identificateurs de deux entrée.</span><span class="sxs-lookup"><span data-stu-id="45c49-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="45c49-114">Si elles ne sont pas les mêmes, définir le contenu du paramètre _lpulResult_ à FALSE et à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="45c49-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="45c49-115">Vérifiez que la taille des identificateurs d’entrée est la taille adéquate pour leur type.</span><span class="sxs-lookup"><span data-stu-id="45c49-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="45c49-116">Si ce n’est pas le cas, le contenu du paramètre _lpulResult_ la valeur False et renvoyer la valeur d’erreur MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="45c49-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="45c49-117">Vérifiez si les identificateurs d’entrée sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="45c49-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="45c49-118">Si elles comparent également, définissez le contenu du paramètre _lpulResult_ sur TRUE et retour.</span><span class="sxs-lookup"><span data-stu-id="45c49-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="45c49-119">Sinon, valeur FALSE avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="45c49-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="45c49-120">Si votre fournisseur compare un identificateur d’entrée à court terme avec un identificateur à long terme, ils doivent également comparer.</span><span class="sxs-lookup"><span data-stu-id="45c49-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

