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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588831"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="3798b-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="3798b-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="3798b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3798b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3798b-105">Supprime prétraités écrites par une fonction [PreprocessMessage](preprocessmessage.md) en fonction d’un message d’informations.</span><span class="sxs-lookup"><span data-stu-id="3798b-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3798b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3798b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3798b-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="3798b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="3798b-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="3798b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3798b-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="3798b-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="3798b-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="3798b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3798b-111">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="3798b-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="3798b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3798b-112">Parameters</span></span>

 <span data-ttu-id="3798b-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3798b-113">_lpMessage_</span></span>
  
> <span data-ttu-id="3798b-114">[in] Pointeur vers le message prétraité à partir duquel les informations sont à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3798b-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3798b-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3798b-115">Return value</span></span>

<span data-ttu-id="3798b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3798b-116">S_OK</span></span>
  
> <span data-ttu-id="3798b-117">Informations prétraitées a été supprimées.</span><span class="sxs-lookup"><span data-stu-id="3798b-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3798b-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="3798b-118">Remarks</span></span>

<span data-ttu-id="3798b-119">Le spouleur MAPI appelle une fonction basée sur **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="3798b-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="3798b-120">Un fournisseur de transport enregistre la fonction **RemovePreprocessInfo** basé en même temps qu’il enregistre la fonction **PreprocessMessage** en parallèle dans un appel à la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="3798b-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="3798b-121">Une image de rendu qui convient pour la transmission de télécopie est un exemple d’information prétraité écrit par une fonction définie par le prototype de fonction [PreprocessMessage](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="3798b-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="3798b-122">Généralement, le spouleur MAPI appelle une fonction **RemovePreprocessInfo** après l’envoi d’un message qui contient des informations prétraitées.</span><span class="sxs-lookup"><span data-stu-id="3798b-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

