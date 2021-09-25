---
title: Ouverture d’une pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ab54b14b9497cd9f1e1bc47bdc2c8d8783db65cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591982"
---
# <a name="opening-an-attachment"></a>Ouverture d’une pièce jointe

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’ouverture d’une pièce jointe implique l’affichage de ses données. Par exemple, lorsqu’une pièce jointe est ouverte, le contenu du fichier s’affiche. Alors que les messages et les dossiers sont ouverts à l’aide de leurs identificateurs d’entrée, les pièces jointes sont ouvertes à l’aide de leurs numéros de pièces jointes **, PR_ATTACH_NUM** propriétés. Pour plus d’informations, **voir PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Les numéros de pièce jointe sont disponibles via la table des pièces jointes d’un message.
  
### <a name="to-open-all-attachments-in-a-message"></a>Pour ouvrir toutes les pièces jointes d’un message
  
1. Appelez la méthode [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) du message pour accéder à sa table de pièces jointes. 
    
2. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes du tableau. 
    
3. Pour chaque ligne : 
    
    1. Ouvrez la pièce jointe en passant le numéro de pièce jointe représenté dans la **colonne PR_ATTACH_NUM** dans un appel à la méthode **IMessage::OpenAttach** du message. Pour plus d’informations, [voir IMessage::OpenAttach](imessage-openattach.md). **OpenAttach renvoie** un pointeur vers une implémentation **IAttach** qui fournit l’accès aux propriétés de pièce jointe. 
        
    2. Appelez la méthode **IMAPIProp::GetProps** de la pièce jointe pour récupérer **PR_ATTACH_METHOD** propriété. Pour plus d’informations, [voir IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Si **PR_ATTACH_METHOD** est définie sur ATTACH_BY_REF_ONLY, appelez **IMAPIProp::GetProps** pour récupérer la **PR_ATTACH_PATHNAME** propriété. Pour plus d’informations, **voir PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Si **la \_ ATTACH_METHOD** pr est définie sur ATTACH BY_VALUE, appelez \_ **IMAPIProp::OpenProperty** pour ouvrir la propriété **pr \_ ATTACH_DATA_BIN** avec l’interface **IStream.** Consultez l’exemple de code suivant cette procédure. Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Si **PR_ATTACH_METHOD** est définie sur ATTACH_OLE et que la pièce jointe est un objet OLE 2 : 
        
        1. Appelez **IMAPIProp::OpenProperty** pour ouvrir la propriété **pr \_ ATTACH_DATA_OBJ** avec l’interface **IStreamDocfile.** Essayez d’utiliser cette interface, car il s’agit d’une implémentation **d’IStream** dont l’utilisation du stockage structuré est garantie avec la charge de travail la moins importante. Pour plus d’informations, **voir PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Si **l’appel OpenProperty** échoue, appelez-le à nouveau pour récupérer la propriété **PR_ATTACH_DATA_BIN** avec l’interface **IStreamDocfile.** 
            
        3. Si ce deuxième **appel OpenProperty** échoue, réessayez d’appeler **OpenProperty** pour récupérer **PR_ATTACH_DATA_OBJ**. Toutefois, au lieu de spécifier **IStreamDocfile**, spécifiez l’interface **IStorage.** 
    
4. Si **PR_ATTACH_METHOD** est définie sur ATTACH_EMBEDDED_MSG, il n’est pas rare que la valeur de PR_ATTACH_DATA_OBJ **contienne** une erreur. Cela est dû au fait que vous et l’implémenteur de table n’avez aucun moyen de vous mettre d’accord sur le type d’objet à renvoyer. Pour récupérer un pointeur vers le message joint, ouvrez la pièce jointe à l’aide **d’IMessage::OpenAttach**. Accédez ensuite aux données de pièce jointe en appelant sa **méthode IMAPIProp::OpenProperty.** Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md) et [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Vous pouvez demander l’ouverture d’une pièce jointe en mode lecture/écriture ou lecture seule. La lecture seule est le mode par défaut, et de nombreux fournisseurs de magasins de messages ouvrent toutes les pièces jointes dans ce mode, quelle que soit la demande des clients. Passez l’indicateur MAPI_BEST_ACCESS pour demander au fournisseur de la boutique de messages d’accorder le niveau d’accès le plus élevé possible, puis récupérez la propriété **PR_ACCESS_LEVEL** de la pièce jointe ouverte pour déterminer le niveau d’accès réellement accordé. Pour plus d’informations, **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
L’exemple suivant montre comment ouvrir les données dans la propriété pr ATTACH_DATA_BIN **d’une \_** pièce jointe. Il alloue des pointeurs à deux flux : un pour le fichier et un pour la pièce jointe. La **fonction OpenStreamOnFile** ouvre le flux de fichiers en mode lecture seule. L’appel à la méthode **IMAPIProp::OpenProperty** de la pièce jointe ouvre le flux de pièce jointe en mode lecture/écriture. Pour plus d’informations, **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)et [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Le code copie ensuite à partir du flux de fichier vers le flux de pièce jointe et libère les deux flux.
  
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


