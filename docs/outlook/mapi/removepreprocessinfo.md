---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432946"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="fc1ff-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="fc1ff-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="fc1ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc1ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc1ff-105">Supprime d’un message les informations prétraitées écrites par une fonction [preprocessMessage.](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="fc1ff-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc1ff-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fc1ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc1ff-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="fc1ff-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="fc1ff-108">Fonction définie implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fc1ff-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="fc1ff-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="fc1ff-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="fc1ff-110">Fonction définie appelée par :</span><span class="sxs-lookup"><span data-stu-id="fc1ff-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="fc1ff-111">Pooler MAPI</span><span class="sxs-lookup"><span data-stu-id="fc1ff-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fc1ff-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fc1ff-112">Parameters</span></span>

 <span data-ttu-id="fc1ff-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="fc1ff-113">_lpMessage_</span></span>
  
> <span data-ttu-id="fc1ff-114">[in] Pointeur vers le message prétraité à partir duquel les informations doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc1ff-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc1ff-115">Return value</span></span>

<span data-ttu-id="fc1ff-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc1ff-116">S_OK</span></span>
  
> <span data-ttu-id="fc1ff-117">Les informations prétraitées ont été supprimées avec succès.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc1ff-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc1ff-118">Remarks</span></span>

<span data-ttu-id="fc1ff-119">Lepooler MAPI appelle une fonction basée sur **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="fc1ff-120">Un fournisseur de transport inscrit la fonction basée **removePreprocessInfo** en même temps qu’il inscrit la fonction **basée sur PreprocessMessage** parallèle dans un appel à la méthode [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md)</span><span class="sxs-lookup"><span data-stu-id="fc1ff-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="fc1ff-121">Un rendu d’image approprié pour la transmission de télécopie est un exemple d’informations prétraitées écrites par une fonction définie par le prototype de fonction [PreprocessMessage.](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="fc1ff-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="fc1ff-122">Lepooler MAPI appelle généralement une **fonction RemovePreprocessInfo** après l’envoi d’un message contenant des informations prétraitées.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

