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
# <a name="removepreprocessinfo"></a><span data-ttu-id="03f7f-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="03f7f-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="03f7f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03f7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03f7f-105">Supprime les informations prétraitées écrites par une fonction basée sur [PreprocessMessage](preprocessmessage.md) à partir d'un message.</span><span class="sxs-lookup"><span data-stu-id="03f7f-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03f7f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="03f7f-106">Header file:</span></span>  <br/> |<span data-ttu-id="03f7f-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="03f7f-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="03f7f-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="03f7f-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="03f7f-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="03f7f-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="03f7f-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="03f7f-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="03f7f-111">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="03f7f-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="03f7f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03f7f-112">Parameters</span></span>

 <span data-ttu-id="03f7f-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="03f7f-113">_lpMessage_</span></span>
  
> <span data-ttu-id="03f7f-114">dans Pointeur vers le message prétraité à partir duquel les informations doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="03f7f-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03f7f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03f7f-115">Return value</span></span>

<span data-ttu-id="03f7f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="03f7f-116">S_OK</span></span>
  
> <span data-ttu-id="03f7f-117">Les informations prétraitées ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="03f7f-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03f7f-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="03f7f-118">Remarks</span></span>

<span data-ttu-id="03f7f-119">Le spouleur MAPI appelle une fonction basée sur **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="03f7f-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="03f7f-120">Un fournisseur de transport enregistre la fonction basée sur **RemovePreprocessInfo** en même temps qu'il enregistre la fonction **PreprocessMessage** en parallèle dans un appel à la méthode [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="03f7f-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="03f7f-121">Un rendu d'image adapté à la transmission de télécopie est un exemple d'informations prétraitées écrites par une fonction définie par le prototype de fonction [PreprocessMessage](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="03f7f-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="03f7f-122">Le spouleur MAPI appelle généralement une fonction **RemovePreprocessInfo** après l'envoi d'un message qui contient des informations prétraitées.</span><span class="sxs-lookup"><span data-stu-id="03f7f-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

