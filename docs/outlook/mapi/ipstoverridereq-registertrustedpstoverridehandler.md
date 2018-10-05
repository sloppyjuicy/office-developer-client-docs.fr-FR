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
description: 'Dernière modification : 24 février 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393872"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="8c579-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="8c579-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="8c579-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c579-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c579-105">Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="8c579-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="8c579-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c579-106">Parameters</span></span>

 <span data-ttu-id="8c579-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="8c579-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="8c579-108">[in] Pointeur vers le chemin d’accès d’une bibliothèque de liens dynamiques (DLL) tiers.</span><span class="sxs-lookup"><span data-stu-id="8c579-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="8c579-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="8c579-109">_pvClientData_</span></span>
  
> <span data-ttu-id="8c579-110">[in] Pointeur vers les données clientes qui sont passés par le fournisseur PST dans les appels suivants à la fonction la DLL HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="8c579-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="8c579-111">Ces données client peuvent être utilisées par la DLL pour vous aider à vérifier si le fichier PST doit être déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="8c579-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8c579-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c579-112">Return value</span></span>

<span data-ttu-id="8c579-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c579-113">S_OK</span></span>
  
> <span data-ttu-id="8c579-114">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="8c579-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c579-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="8c579-115">Remarks</span></span>

<span data-ttu-id="8c579-116">La DLL spécifiée par le paramètre wzDllPath doit être signée à l’aide d’un certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="8c579-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="8c579-117">La DLL doit également exporter une fonction avec la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="8c579-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="8c579-118">Cette fonction est appelée avec un pointeur vers l’objet IMsgStore pour le fichier PST, un pointeur vers un objet IUnknown qui implémente l’interface IPSTOVERRIDE1 et un pointeur vers les données fournies par le biais de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="8c579-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="8c579-119">Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="8c579-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c579-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c579-120">See also</span></span>



[<span data-ttu-id="8c579-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c579-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="8c579-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c579-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

