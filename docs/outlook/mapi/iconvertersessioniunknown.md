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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 316e17e7804e754eed4ee4fef27211fb5173d4bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589643"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="9884f-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9884f-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="9884f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9884f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9884f-105">Permet les conversions entre objets MIME et les messages MAPI.</span><span class="sxs-lookup"><span data-stu-id="9884f-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="9884f-106">Cela peut être utile de transport des messages via Internet.</span><span class="sxs-lookup"><span data-stu-id="9884f-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9884f-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="9884f-107">Provided by:</span></span>  <br/> |<span data-ttu-id="9884f-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="9884f-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="9884f-109">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="9884f-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9884f-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="9884f-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9884f-111">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="9884f-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9884f-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="9884f-113">Spécifie une option carnet d’adresses MAPI par l’interface MAPI convertisseur MIME pour résoudre les adresses ambigus lors de la conversion d’un message MAPI à un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="9884f-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="9884f-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="9884f-115">Initialise le codage à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="9884f-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="9884f-116">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="9884f-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9884f-117">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="9884f-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9884f-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="9884f-119">Convertit un flux de données MIME à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="9884f-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9884f-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="9884f-121">Convertit un message MAPI à un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="9884f-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="9884f-122">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="9884f-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9884f-123">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="9884f-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9884f-124">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="9884f-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9884f-125">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="9884f-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9884f-126">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="9884f-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9884f-127">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="9884f-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9884f-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="9884f-129">Définit la largeur d’un flux MIME qui retourne le convertisseur **MAPIToMIMEStm**d’habillage de texte.</span><span class="sxs-lookup"><span data-stu-id="9884f-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="9884f-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="9884f-131">Définit le format que le convertisseur retourne un flux de données MIME dans **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="9884f-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="9884f-132">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="9884f-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9884f-133">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="9884f-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9884f-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="9884f-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="9884f-135">Spécifie un caractère facultatif que l’interface MAPI convertisseur MIME utilise lors de la conversion d’un message MAPI à un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="9884f-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9884f-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="9884f-136">Remarks</span></span>

<span data-ttu-id="9884f-137">Appelez **SetEncoding** avant d’utiliser **MAPIToMIMEStm** pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="9884f-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9884f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9884f-138">See also</span></span>



[<span data-ttu-id="9884f-139">À propos de l’API de conversion MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="9884f-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="9884f-140">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9884f-140">MAPI Constants</span></span>](mapi-constants.md)

