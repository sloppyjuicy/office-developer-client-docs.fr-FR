---
title: Ouverture d’une pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430622"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="3c97d-103">Ouverture d’une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="3c97d-103">Opening an attachment</span></span>

<span data-ttu-id="3c97d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c97d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c97d-105">L’ouverture d’une pièce jointe implique l’affichage de ses données.</span><span class="sxs-lookup"><span data-stu-id="3c97d-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="3c97d-106">Par exemple, lorsqu’une pièce jointe est ouverte, le contenu du fichier s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3c97d-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="3c97d-107">Alors que les messages et les dossiers sont ouverts à l’aide de leurs identificateurs d’entrée, les pièces jointes sont ouvertes à l’aide de leurs numéros de pièces jointes **, PR_ATTACH_NUM** propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c97d-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="3c97d-108">Pour plus d’informations, **voir PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c97d-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="3c97d-109">Les numéros de pièce jointe sont disponibles via la table des pièces jointes d’un message.</span><span class="sxs-lookup"><span data-stu-id="3c97d-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="3c97d-110">Pour ouvrir toutes les pièces jointes d’un message</span><span class="sxs-lookup"><span data-stu-id="3c97d-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="3c97d-111">Appelez la méthode [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) du message pour accéder à sa table de pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="3c97d-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="3c97d-112">Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="3c97d-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="3c97d-113">Pour chaque ligne :</span><span class="sxs-lookup"><span data-stu-id="3c97d-113">For each row:</span></span> 
    
    1. <span data-ttu-id="3c97d-114">Ouvrez la pièce jointe en passant le numéro de pièce jointe représenté dans la **colonne PR_ATTACH_NUM** dans un appel à la méthode **IMessage::OpenAttach** du message.</span><span class="sxs-lookup"><span data-stu-id="3c97d-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="3c97d-115">Pour plus d’informations, [voir IMessage::OpenAttach](imessage-openattach.md).</span><span class="sxs-lookup"><span data-stu-id="3c97d-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="3c97d-116">**OpenAttach renvoie** un pointeur vers une implémentation **IAttach** qui fournit l’accès aux propriétés de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3c97d-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="3c97d-117">Appelez la méthode **IMAPIProp::GetProps** de la pièce jointe pour récupérer **sa PR_ATTACH_METHOD** jointe.</span><span class="sxs-lookup"><span data-stu-id="3c97d-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="3c97d-118">Pour plus d’informations, [voir IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c97d-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="3c97d-119">Si **PR_ATTACH_METHOD** est définie sur ATTACH_BY_REF_ONLY, appelez **IMAPIProp::GetProps** pour récupérer la **PR_ATTACH_PATHNAME** propriété.</span><span class="sxs-lookup"><span data-stu-id="3c97d-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="3c97d-120">Pour plus d’informations, **voir PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c97d-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="3c97d-121">Si **la \_ ATTACH_METHOD** pr est définie sur ATTACH BY_VALUE, appelez \_ **IMAPIProp::OpenProperty** pour ouvrir la propriété **pr \_ ATTACH_DATA_BIN** avec l’interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="3c97d-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="3c97d-122">Consultez l’exemple de code suivant cette procédure.</span><span class="sxs-lookup"><span data-stu-id="3c97d-122">See the sample code following this procedure.</span></span> <span data-ttu-id="3c97d-123">Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c97d-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="3c97d-124">Si **PR_ATTACH_METHOD** est définie sur ATTACH_OLE et que la pièce jointe est un objet OLE 2 :</span><span class="sxs-lookup"><span data-stu-id="3c97d-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="3c97d-125">Appelez **IMAPIProp::OpenProperty** pour ouvrir la propriété **pr \_ ATTACH_DATA_OBJ** avec l’interface **IStreamDocfile.**</span><span class="sxs-lookup"><span data-stu-id="3c97d-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="3c97d-126">Essayez d’utiliser cette interface, car il s’agit d’une implémentation **d’IStream** dont l’utilisation du stockage structuré est garantie avec le moins de surcharge.</span><span class="sxs-lookup"><span data-stu-id="3c97d-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="3c97d-127">Pour plus d’informations, **voir PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c97d-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="3c97d-128">Si **l’appel OpenProperty** échoue, appelez-le à nouveau pour récupérer la propriété **PR_ATTACH_DATA_BIN** avec l’interface **IStreamDocfile.**</span><span class="sxs-lookup"><span data-stu-id="3c97d-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="3c97d-129">Si ce deuxième **appel OpenProperty** échoue, réessayez d’appeler **OpenProperty** pour récupérer **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="3c97d-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="3c97d-130">Toutefois, au lieu de spécifier **IStreamDocfile**, spécifiez l’interface **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="3c97d-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="3c97d-131">Si **PR_ATTACH_METHOD** est définie sur ATTACH_EMBEDDED_MSG, il n’est pas rare que la valeur de PR_ATTACH_DATA_OBJ **contienne** une erreur.</span><span class="sxs-lookup"><span data-stu-id="3c97d-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="3c97d-132">Cela est dû au fait que vous et l’implémenteur de table n’avez aucun moyen de vous mettre d’accord sur le type d’objet à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="3c97d-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="3c97d-133">Pour récupérer un pointeur vers le message joint, ouvrez la pièce jointe à l’aide **d’IMessage::OpenAttach**.</span><span class="sxs-lookup"><span data-stu-id="3c97d-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="3c97d-134">Accédez ensuite aux données de pièce jointe en appelant sa **méthode IMAPIProp::OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="3c97d-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="3c97d-135">Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md) et [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3c97d-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="3c97d-136">Vous pouvez demander l’ouverture d’une pièce jointe en mode lecture/écriture ou lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3c97d-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="3c97d-137">La lecture seule est le mode par défaut, et de nombreux fournisseurs de magasins de messages ouvrent toutes les pièces jointes dans ce mode, quelle que soit la demande des clients.</span><span class="sxs-lookup"><span data-stu-id="3c97d-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="3c97d-138">Passez l’indicateur MAPI_BEST_ACCESS pour demander au fournisseur de la boutique de messages d’accorder le niveau d’accès le plus élevé possible, puis récupérez la propriété **PR_ACCESS_LEVEL** de la pièce jointe ouverte pour déterminer le niveau d’accès réellement accordé.</span><span class="sxs-lookup"><span data-stu-id="3c97d-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="3c97d-139">Pour plus d’informations, **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c97d-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="3c97d-140">L’exemple suivant montre comment ouvrir les données dans la propriété pr ATTACH_DATA_BIN **d’une \_** pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3c97d-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="3c97d-141">Il alloue des pointeurs à deux flux : un pour le fichier et un pour la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3c97d-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="3c97d-142">La **fonction OpenStreamOnFile** ouvre le flux de fichiers en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3c97d-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="3c97d-143">L’appel à la méthode **IMAPIProp::OpenProperty** de la pièce jointe ouvre le flux de pièce jointe en mode lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3c97d-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="3c97d-144">Pour plus d’informations, **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)et [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3c97d-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="3c97d-145">Le code copie ensuite à partir du flux de fichier vers le flux de pièce jointe et libère les deux flux.</span><span class="sxs-lookup"><span data-stu-id="3c97d-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
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


