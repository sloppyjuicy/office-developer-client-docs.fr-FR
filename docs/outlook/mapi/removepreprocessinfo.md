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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787018"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="577e4-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="577e4-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="577e4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="577e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="577e4-105">Supprime prétraités écrites par une fonction [PreprocessMessage](preprocessmessage.md) en fonction d’un message d’informations.</span><span class="sxs-lookup"><span data-stu-id="577e4-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="577e4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="577e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="577e4-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="577e4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="577e4-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="577e4-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="577e4-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="577e4-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="577e4-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="577e4-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="577e4-111">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="577e4-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="577e4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="577e4-112">Parameters</span></span>

 <span data-ttu-id="577e4-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="577e4-113">_lpMessage_</span></span>
  
> <span data-ttu-id="577e4-114">[in] Pointeur vers le message prétraité à partir duquel les informations sont à supprimer.</span><span class="sxs-lookup"><span data-stu-id="577e4-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="577e4-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="577e4-115">Return value</span></span>

<span data-ttu-id="577e4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="577e4-116">S_OK</span></span>
  
> <span data-ttu-id="577e4-117">Informations prétraitées a été supprimées.</span><span class="sxs-lookup"><span data-stu-id="577e4-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="577e4-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="577e4-118">Remarks</span></span>

<span data-ttu-id="577e4-119">Le spouleur MAPI appelle une fonction basée sur **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="577e4-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="577e4-120">Un fournisseur de transport enregistre la fonction **RemovePreprocessInfo** basé en même temps qu’il enregistre la fonction **PreprocessMessage** en parallèle dans un appel à la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="577e4-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="577e4-121">Une image de rendu qui convient pour la transmission de télécopie est un exemple d’information prétraité écrit par une fonction définie par le prototype de fonction [PreprocessMessage](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="577e4-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="577e4-122">Généralement, le spouleur MAPI appelle une fonction **RemovePreprocessInfo** après l’envoi d’un message qui contient des informations prétraitées.</span><span class="sxs-lookup"><span data-stu-id="577e4-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

