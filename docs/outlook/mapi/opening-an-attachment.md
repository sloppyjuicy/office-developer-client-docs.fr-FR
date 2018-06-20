---
title: L’ouverture d’une pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3875e51868e882ca454c06949347327a21a93eb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784924"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="d028b-103">L’ouverture d’une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="d028b-103">Opening an attachment</span></span>

<span data-ttu-id="d028b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d028b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d028b-105">L’ouverture d’une pièce jointe implique l’affichage de ses données.</span><span class="sxs-lookup"><span data-stu-id="d028b-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="d028b-106">Par exemple, lorsqu’une pièce jointe est ouvert, affiche le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="d028b-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="d028b-107">Tandis que les messages et les dossiers sont ouverts à l’aide de leurs identificateurs d’entrée, les pièces jointes sont ouvertes à l’aide de leurs numéros de pièce jointe, propriétés **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="d028b-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="d028b-108">Pour plus d’informations, voir **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d028b-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="d028b-109">Les numéros de pièce jointe sont disponibles via la table des pièces jointes d’un message.</span><span class="sxs-lookup"><span data-stu-id="d028b-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="d028b-110">Pour ouvrir toutes les pièces jointes dans un message</span><span class="sxs-lookup"><span data-stu-id="d028b-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="d028b-111">Appeler la méthode de [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) du message pour accéder à la table des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="d028b-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="d028b-112">Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d028b-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="d028b-113">Pour chaque ligne :</span><span class="sxs-lookup"><span data-stu-id="d028b-113">For each row:</span></span> 
    
    1. <span data-ttu-id="d028b-114">Ouvrez la pièce jointe en transmettant le numéro de pièce jointe représenté dans la colonne **PR_ATTACH_NUM** dans un appel à la méthode **IMessage::OpenAttach** du message.</span><span class="sxs-lookup"><span data-stu-id="d028b-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="d028b-115">Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md).</span><span class="sxs-lookup"><span data-stu-id="d028b-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="d028b-116">**OpenAttach** retourne un pointeur vers une implémentation **IAttach** qui fournit l’accès aux propriétés de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d028b-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="d028b-117">Appelez la méthode de **IMAPIProp::GetProps** de la pièce jointe pour récupérer sa propriété **PR_ATTACH_METHOD** .</span><span class="sxs-lookup"><span data-stu-id="d028b-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="d028b-118">Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d028b-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="d028b-119">Si **PR_ATTACH_METHOD** est défini sur ATTACH_BY_REF_ONLY, appelez **IMAPIProp::GetProps** pour récupérer la propriété **PR_ATTACH_PATHNAME** .</span><span class="sxs-lookup"><span data-stu-id="d028b-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="d028b-120">Pour plus d’informations, voir **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d028b-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="d028b-121">Si **PR\_ATTACH_METHOD** est défini sur ATTACH\_BY_VALUE, appelez **IMAPIProp::OpenProperty** pour ouvrir le **PR\_ATTACH_DATA_BIN** propriété avec l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="d028b-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="d028b-122">Voir l’exemple de code qui suit cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d028b-122">See the sample code following this procedure.</span></span> <span data-ttu-id="d028b-123">Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d028b-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="d028b-124">Si **PR_ATTACH_METHOD** est défini sur ATTACH_OLE et la pièce jointe est un objet OLE 2 :</span><span class="sxs-lookup"><span data-stu-id="d028b-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="d028b-125">Appelez **IMAPIProp::OpenProperty** pour ouvrir le **PR\_ATTACH_DATA_OBJ** propriété avec l’interface **IStreamDocfile** .</span><span class="sxs-lookup"><span data-stu-id="d028b-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="d028b-126">Essayez d’utiliser cette interface, car il s’agit d’une implémentation **IStream** fonctionnent avec le stockage structuré avec le moins de surcharge.</span><span class="sxs-lookup"><span data-stu-id="d028b-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="d028b-127">Pour plus d’informations, voir **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d028b-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="d028b-128">Si l’appel **OpenProperty** échoue, appelez à nouveau pour récupérer la propriété **PR_ATTACH_DATA_BIN** avec l’interface **IStreamDocfile** .</span><span class="sxs-lookup"><span data-stu-id="d028b-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="d028b-129">Si ce deuxième appel **OpenProperty** échoue, essayez à nouveau d’appeler **OpenProperty** pour récupérer **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="d028b-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="d028b-130">Toutefois, au lieu de spécifier **IStreamDocfile**, spécifiez l’interface **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="d028b-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="d028b-131">Si **PR_ATTACH_METHOD** est défini sur ATTACH_EMBEDDED_MSG, il n’est pas rare que la valeur de **PR_ATTACH_DATA_OBJ** contenant une erreur.</span><span class="sxs-lookup"><span data-stu-id="d028b-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="d028b-132">C’est pourquoi vous et l’implémentation de la table n’ont aucun moyen d’accord sur le type d’objet à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="d028b-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="d028b-133">Pour récupérer un pointeur vers le message joint, ouvrez la pièce jointe à l’aide de **IMessage::OpenAttach**.</span><span class="sxs-lookup"><span data-stu-id="d028b-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="d028b-134">Puis accéder aux données de pièce jointe en appelant la méthode **IMAPIProp::OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="d028b-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="d028b-135">Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md) et [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d028b-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="d028b-136">Vous pouvez demander qu’une pièce jointe est ouvert en lecture/écriture ou en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d028b-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="d028b-137">En lecture seule est le mode par défaut, et de nombreux fournisseurs de banque de messages ouvrent toutes les pièces jointes dans ce mode, quelle que soit la demandent de clients.</span><span class="sxs-lookup"><span data-stu-id="d028b-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="d028b-138">Passer l’indicateur MAPI_BEST_ACCESS pour demander que le fournisseur de banque de messages accorder le niveau d’accès, il peut et d’extraire ensuite la propriété **PR_ACCESS_LEVEL** de la pièce jointe open pour déterminer le niveau d’accès qui a été reçu le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="d028b-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="d028b-139">Pour plus d’informations, voir **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d028b-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="d028b-140">L’exemple suivant montre comment ouvrir les données dans la pièce jointe **PR\_ATTACH_DATA_BIN** propriété.</span><span class="sxs-lookup"><span data-stu-id="d028b-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="d028b-141">Il alloue des pointeurs vers deux flux : un pour le fichier et un pour la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d028b-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="d028b-142">La fonction **OpenStreamOnFile** ouvre le flux de fichier en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d028b-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="d028b-143">L’appel à **IMAPIProp::OpenProperty** méthode la pièce jointe ouvre le flux de pièces jointes en mode lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d028b-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="d028b-144">Pour plus d’informations, voir **PR_ATTACH_DATA_BIN**et [IMAPIProp::OpenProperty](imapiprop-openproperty.md) [OpenStreamOnFile](openstreamonfile.md).</span><span class="sxs-lookup"><span data-stu-id="d028b-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="d028b-145">Le code puis copie à partir du flux de fichier dans le flux de pièces jointes et libère les deux flux.</span><span class="sxs-lookup"><span data-stu-id="d028b-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


