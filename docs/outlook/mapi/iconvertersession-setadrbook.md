---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326893"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="09650-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="09650-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="09650-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09650-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09650-105">Spécifie un carnet d'adresses MAPI facultatif que le convertisseur MAPI vers MIME utilise pour résoudre des adresses ambiguës lors de la conversion d'un message MAPI en un flux MIME.</span><span class="sxs-lookup"><span data-stu-id="09650-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="09650-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09650-106">Parameters</span></span>

 <span data-ttu-id="09650-107">_Cap_</span><span class="sxs-lookup"><span data-stu-id="09650-107">_pab_</span></span>
  
> <span data-ttu-id="09650-108">dans Pointeur vers une interface [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) à utiliser dans la conversion MAPI vers MIME.</span><span class="sxs-lookup"><span data-stu-id="09650-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="09650-109">Définissez ce paramètre sur **null** lorsque vous n'avez plus besoin du carnet d'adresses; Cela libère l'interface et réinitialise le convertisseur de sorte qu'il n'utilise aucun carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="09650-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09650-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="09650-110">Return value</span></span>

<span data-ttu-id="09650-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="09650-111">S_OK</span></span>
  
> <span data-ttu-id="09650-112">L'appel de fonction est réussi.</span><span class="sxs-lookup"><span data-stu-id="09650-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09650-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="09650-113">Remarks</span></span>

<span data-ttu-id="09650-114">La conversion d'un message MAPI en flux MIME n'exige généralement pas l'ouverture d'une session sur un profil MAPI.</span><span class="sxs-lookup"><span data-stu-id="09650-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="09650-115">Toutefois, si vous spécifiez un carnet d'adresses MAPI pour la conversion, vous devez vous connecter à un profil pour obtenir le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="09650-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09650-116">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="09650-116">MFCMAPI reference</span></span>

<span data-ttu-id="09650-117">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="09650-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09650-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="09650-118">**File**</span></span>|<span data-ttu-id="09650-119">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="09650-119">**Function**</span></span>|<span data-ttu-id="09650-120">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="09650-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09650-121">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="09650-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="09650-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="09650-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="09650-123">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="09650-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="09650-124">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="09650-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="09650-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="09650-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="09650-126">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="09650-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09650-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09650-127">See also</span></span>



[<span data-ttu-id="09650-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09650-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="09650-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="09650-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="09650-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="09650-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="09650-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="09650-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="09650-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="09650-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="09650-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="09650-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="09650-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="09650-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

