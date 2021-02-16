---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Last modified: February 24, 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279534"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="e99d1-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e99d1-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="e99d1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e99d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e99d1-105">Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="e99d1-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="e99d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e99d1-106">Parameters</span></span>

 <span data-ttu-id="e99d1-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="e99d1-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="e99d1-108">[in] Pointeur vers le chemin d’accès d’une bibliothèque de liens dynamiques (DLL) tierce.</span><span class="sxs-lookup"><span data-stu-id="e99d1-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="e99d1-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="e99d1-109">_pvClientData_</span></span>
  
> <span data-ttu-id="e99d1-110">[in] Pointeur vers les données client, qui seront transmises par le fournisseur PST dans les appels ultérieurs à la fonction HrTrustedPSTOverrideHandlerCallback de la DLL.</span><span class="sxs-lookup"><span data-stu-id="e99d1-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="e99d1-111">Ces données client peuvent être utilisées par la DLL pour vous aider à vérifier si le PST doit être déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="e99d1-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e99d1-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e99d1-112">Return value</span></span>

<span data-ttu-id="e99d1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e99d1-113">S_OK</span></span>
  
> <span data-ttu-id="e99d1-114">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="e99d1-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e99d1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e99d1-115">Remarks</span></span>

<span data-ttu-id="e99d1-116">La DLL spécifiée par le paramètre wzDllPath doit être signée à l’aide d’un certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="e99d1-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="e99d1-117">La DLL doit également exporter une fonction avec la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="e99d1-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="e99d1-118">Cette fonction est appelée avec un pointeur vers l’objet IMsgStore pour le PST, un pointeur vers un objet IUnknown qui implémente l’interface IPSTOVERRIDE1 et un pointeur vers les données fournies à l’origine par pvClientData.</span><span class="sxs-lookup"><span data-stu-id="e99d1-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="e99d1-119">Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="e99d1-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e99d1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e99d1-120">See also</span></span>



[<span data-ttu-id="e99d1-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e99d1-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="e99d1-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e99d1-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

