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
# <a name="opening-an-attachment"></a>L’ouverture d’une pièce jointe

**S’applique à**: Outlook 
  
L’ouverture d’une pièce jointe implique l’affichage de ses données. Par exemple, lorsqu’une pièce jointe est ouvert, affiche le contenu du fichier. Tandis que les messages et les dossiers sont ouverts à l’aide de leurs identificateurs d’entrée, les pièces jointes sont ouvertes à l’aide de leurs numéros de pièce jointe, propriétés **PR_ATTACH_NUM** . Pour plus d’informations, voir **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Les numéros de pièce jointe sont disponibles via la table des pièces jointes d’un message.
  
### <a name="to-open-all-attachments-in-a-message"></a>Pour ouvrir toutes les pièces jointes dans un message
  
1. Appeler la méthode de [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) du message pour accéder à la table des pièces jointes. 
    
2. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes dans le tableau. 
    
3. Pour chaque ligne : 
    
    1. Ouvrez la pièce jointe en transmettant le numéro de pièce jointe représenté dans la colonne **PR_ATTACH_NUM** dans un appel à la méthode **IMessage::OpenAttach** du message. Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** retourne un pointeur vers une implémentation **IAttach** qui fournit l’accès aux propriétés de la pièce jointe. 
        
    2. Appelez la méthode de **IMAPIProp::GetProps** de la pièce jointe pour récupérer sa propriété **PR_ATTACH_METHOD** . Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Si **PR_ATTACH_METHOD** est défini sur ATTACH_BY_REF_ONLY, appelez **IMAPIProp::GetProps** pour récupérer la propriété **PR_ATTACH_PATHNAME** . Pour plus d’informations, voir **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Si **PR\_ATTACH_METHOD** est défini sur ATTACH\_BY_VALUE, appelez **IMAPIProp::OpenProperty** pour ouvrir le **PR\_ATTACH_DATA_BIN** propriété avec l’interface **IStream** . Voir l’exemple de code qui suit cette procédure. Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Si **PR_ATTACH_METHOD** est défini sur ATTACH_OLE et la pièce jointe est un objet OLE 2 : 
        
        1. Appelez **IMAPIProp::OpenProperty** pour ouvrir le **PR\_ATTACH_DATA_OBJ** propriété avec l’interface **IStreamDocfile** . Essayez d’utiliser cette interface, car il s’agit d’une implémentation **IStream** fonctionnent avec le stockage structuré avec le moins de surcharge. Pour plus d’informations, voir **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Si l’appel **OpenProperty** échoue, appelez à nouveau pour récupérer la propriété **PR_ATTACH_DATA_BIN** avec l’interface **IStreamDocfile** . 
            
        3. Si ce deuxième appel **OpenProperty** échoue, essayez à nouveau d’appeler **OpenProperty** pour récupérer **PR_ATTACH_DATA_OBJ**. Toutefois, au lieu de spécifier **IStreamDocfile**, spécifiez l’interface **IStorage** . 
    
4. Si **PR_ATTACH_METHOD** est défini sur ATTACH_EMBEDDED_MSG, il n’est pas rare que la valeur de **PR_ATTACH_DATA_OBJ** contenant une erreur. C’est pourquoi vous et l’implémentation de la table n’ont aucun moyen d’accord sur le type d’objet à renvoyer. Pour récupérer un pointeur vers le message joint, ouvrez la pièce jointe à l’aide de **IMessage::OpenAttach**. Puis accéder aux données de pièce jointe en appelant la méthode **IMAPIProp::OpenProperty** . Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md) et [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Vous pouvez demander qu’une pièce jointe est ouvert en lecture/écriture ou en lecture seule. En lecture seule est le mode par défaut, et de nombreux fournisseurs de banque de messages ouvrent toutes les pièces jointes dans ce mode, quelle que soit la demandent de clients. Passer l’indicateur MAPI_BEST_ACCESS pour demander que le fournisseur de banque de messages accorder le niveau d’accès, il peut et d’extraire ensuite la propriété **PR_ACCESS_LEVEL** de la pièce jointe open pour déterminer le niveau d’accès qui a été reçu le plus élevé. Pour plus d’informations, voir **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
L’exemple suivant montre comment ouvrir les données dans la pièce jointe **PR\_ATTACH_DATA_BIN** propriété. Il alloue des pointeurs vers deux flux : un pour le fichier et un pour la pièce jointe. La fonction **OpenStreamOnFile** ouvre le flux de fichier en mode lecture seule. L’appel à **IMAPIProp::OpenProperty** méthode la pièce jointe ouvre le flux de pièces jointes en mode lecture/écriture. Pour plus d’informations, voir **PR_ATTACH_DATA_BIN**et [IMAPIProp::OpenProperty](imapiprop-openproperty.md) [OpenStreamOnFile](openstreamonfile.md). Le code puis copie à partir du flux de fichier dans le flux de pièces jointes et libère les deux flux.
  
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


