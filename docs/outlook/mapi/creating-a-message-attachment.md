---
title: Création d’une pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 34d8dbeaf101d5ebb687403a2200bd0ad73b9998
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577099"
---
# <a name="creating-a-message-attachment"></a>Création d’une pièce jointe
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une pièce jointe du message est certaines données supplémentaires, comme un fichier, un autre message ou un objet OLE, que vous pouvez envoyer ou enregistrer avec un message. Chaque pièce jointe est une collection de propriétés qui identifie et décrit le type et la façon dont il s’affiche. Comme destinataires, pièces jointes des messages uniquement accessible via le message auquel ils appartiennent. Par conséquent, pour une pièce jointe utilisable, son message doit être ouvert.
  
## <a name="create-a-message-attachment"></a>Créer une pièce jointe
  
1. Appelez la méthode [IMessage::CreateAttach](imessage-createattach.md) du message et passer la valeur NULL en tant que l’identificateur d’interface. **CreateAttach** renvoie un numéro qui identifie de manière unique la nouvelle pièce jointe du message. Le nombre de pièces jointes est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) et est valide uniquement tant que le message contenant la pièce jointe est ouvert.
    
2. Appelez [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) pour indiquer comment accéder à la pièce jointe. **PR_ATTACH_METHOD** est requis. Affectez-lui la valeur : 
    
   - ATTACH_BY_VALUE s’il s’agit des données binaires.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY si la pièce jointe est un fichier.
    
   - ATTACH_EMBEDDED_MSG si la pièce jointe est un message.
    
   - ATTACH_OLE si la pièce jointe est un objet OLE.
    
3. Définissez la propriété de données de pièce jointe approprié :
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) pour les données binaires et les objets OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) pour les fichiers.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) pour les messages et les objets OLE 2.
    
4. Définissez **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) pour contenir la représentation graphique de la pièce jointe de fichier ou de pièces jointes binaires. Ne le définissez pas pour les objets OLE, qui stockent les informations de rendu en interne, ou pour les messages attachés. 
    
5. Définissez **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) pour indiquer où la pièce jointe doit être affichée. **PR_RENDERING_POSITION** s’applique uniquement aux clients qui définissent la propriété **PR_BODY** . Si vous ne prennent en charge **PR_RTF_COMPRESSED**, placez les informations d’espace réservé suivantes dans le flux compressé :
    
   `\objattph`

   Pour définir **PR_RENDERING_POSITION**, attribuer soit un numéro qui représente un décalage ordinal en caractères, avec le premier caractère de **PR_BODY** étant égale à 0, si vous avez besoin de savoir où dans le message de la pièce jointe est restituée ou 0xFFFFFFFF, si vous le faites pas afficher les pièces jointes dans **PR_BODY**.
    
6. Définir **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) pour indiquer le nom court du fichier d’une pièce jointe et **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) pour indiquer le nom du fichier de prise en charge sur une plateforme qui gère le format de nom de fichier long. Les deux propriétés sont facultatives. Toutefois, si vous définissez **PR_ATTACH_LONG_FILENAME**, définissez également **PR_ATTACH_FILENAME**. 
    
7. Définissez **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) pour indiquer le nom de la pièce jointe qui peut apparaître dans une boîte de dialogue. PR_DISPLAY_NAME est facultative. 
    
## <a name="set-prattachdatabin"></a>Définir PR_ATTACH_DATA_BIN
  
1. Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété avec l’interface **IStream** . 
    
2. Si un fichier contient les données et il est ouvert ou si vous avez besoin de contrôle explicite sur la taille de la mémoire tampon, appelez **IStream::Write** dans une boucle pour placer les données dans le flux. 
    
3. Une autre option consiste à appeler **OpenStreamOnFile** pour créer un flux de données pour accéder au fichier de données et ensuite appeler la méthode de **IStream::CopyTo** de ce flux pour copier les données dans le flux retourné par **OpenProperty**.
    
4. Appeler la nouvelle méthode du flux **IStream::Commit** . 
    
## <a name="set-prattachdataobj"></a>Définir PR_ATTACH_DATA_OBJ
  
1. Appelez **IMAPIProp::OpenProperty** pour ouvrir la propriété avec l’interface **IStreamDocfile** pour créer un flux de données qui fonctionne avec le stockage structuré. **IStreamDocfile** est implémentée par les fournisseurs de banque de messages de donner aux clients un moyen de meilleures performances pour stocker et récupérer du stockage structuré. L’interface **IStreamDocfile** est la même que **IStream**, mais le contenu de l’objet stream est systématiquement à mettre en forme en tant que stockage structuré. Si cet appel aboutit, créer le flux de données avec les mêmes étapes décrites pour le paramètre **PR_ATTACH_DATA_BIN**.
    
2. En cas d’échec de **OpenProperty** : 
    
   1. Appelez **OpenProperty** **IStorage**demandant à nouveau. 
      
   2. Appelez **StgOpenStorage** pour ouvrir l’objet OLE et de renvoyer un objet de stockage. 
      
   3. Appelez le stockage renvoyé **IStorage::CopyTo** méthode objet à copier vers l’objet de stockage renvoyé par **OpenProperty**.
      
   4. Appeler la méthode de **IStorage::Commit** du nouvel objet stockage. 
    
## <a name="set-prattachpathname"></a>Définir PR_ATTACH_PATHNAME
  
1. Allouez une structure [SPropValue](spropvalue.md) , attribuez au membre **ulPropTag** **PR_ATTACH_PATHNAME** et le membre **Value.LPSZ** la chaîne de caractères représentant le nom de fichier. 
    
2. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la pièce jointe. 
    
> [!NOTE]
> Si votre plate-forme prend en charge les noms de fichiers longs, définissez à la fois **PR_ATTACH_PATHNAME** et **PR_ATTACH_LONG_PATHNAME**. Il peut être nécessaire appeler un système d’exploitation pour extraire le nom de fichier court. 
  
## <a name="see-also"></a>Voir aussi

- [Pi�ces jointes MAPI](mapi-attachments.md)

