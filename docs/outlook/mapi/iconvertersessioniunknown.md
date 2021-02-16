---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432316"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="02424-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02424-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="02424-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02424-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02424-105">Autorise les conversions entre les objets MIME et les messages MAPI.</span><span class="sxs-lookup"><span data-stu-id="02424-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="02424-106">Cela peut être utile pour le transport de messages sur Internet.</span><span class="sxs-lookup"><span data-stu-id="02424-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02424-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="02424-107">Provided by:</span></span>  <br/> |<span data-ttu-id="02424-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="02424-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="02424-109">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="02424-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="02424-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="02424-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="02424-111">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="02424-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02424-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="02424-113">Spécifie un carnet d’adresses MAPI facultatif que le convertisseur MAPI en MIME utilise pour résoudre des adresses ambiguës lors de la conversion d’un message MAPI en flux MIME.</span><span class="sxs-lookup"><span data-stu-id="02424-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="02424-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="02424-115">Initialise le codage à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="02424-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="02424-116">*Membre d’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="02424-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="02424-117">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="02424-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="02424-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="02424-119">Convertit un flux MIME en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="02424-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="02424-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="02424-121">Convertit un message MAPI en flux MIME.</span><span class="sxs-lookup"><span data-stu-id="02424-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="02424-122">*Membre d’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="02424-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="02424-123">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="02424-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="02424-124">*Membre d’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="02424-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="02424-125">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="02424-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="02424-126">*Membre d’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="02424-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="02424-127">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="02424-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="02424-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="02424-129">Définit la largeur du retour à la ligne pour un flux MIME que le convertisseur renvoie dans **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="02424-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="02424-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="02424-131">Définit le format que le convertisseur renvoie un flux MIME dans **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="02424-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="02424-132">*Membre d’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="02424-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="02424-133">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="02424-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="02424-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="02424-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="02424-135">Spécifie un jeu de caractères facultatif que le convertisseur MAPI en MIME utilise lors de la conversion d’un message MAPI en flux MIME.</span><span class="sxs-lookup"><span data-stu-id="02424-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02424-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="02424-136">Remarks</span></span>

<span data-ttu-id="02424-137">Appelez **SetEncoding avant** d’utiliser **MAPIToMIMEStm** pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="02424-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02424-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02424-138">See also</span></span>



[<span data-ttu-id="02424-139">À propos de l’API de conversion MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="02424-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="02424-140">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="02424-140">MAPI Constants</span></span>](mapi-constants.md)

