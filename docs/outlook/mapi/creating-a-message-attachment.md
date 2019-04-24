---
title: Création d’une pièce jointe de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332941"
---
# <a name="creating-a-message-attachment"></a>Création d’une pièce jointe de message
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une pièce jointe est une donnée supplémentaire, telle qu'un fichier, un autre message ou un objet OLE, que vous pouvez envoyer ou enregistrer avec un message. Chaque pièce jointe possède une collection de propriétés qui l'identifient et décrit son type et son mode d'affichage. Comme pour les destinataires, les pièces jointes des messages sont accessibles uniquement par le biais du message auquel elles appartiennent. Par conséquent, pour qu'une pièce jointe soit utilisable, son message doit être ouvert.
  
## <a name="create-a-message-attachment"></a>Créer une pièce jointe de message
  
1. Appelez la méthode [IMessage:: CreateAttach](imessage-createattach.md) du message et transmettez la valeur NULL comme identificateur d'interface. **CreateAttach** renvoie un numéro qui identifie de manière unique la nouvelle pièce jointe dans le message. Le numéro de pièce jointe est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) et est valide uniquement tant que le message contenant la pièce jointe est ouvert.
    
2. Appelez [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) afin d'indiquer comment accéder à la pièce jointe. **PR_ATTACH_METHOD** est obligatoire. Définissez-la sur: 
    
   - ATTACH_BY_VALUE si la pièce jointe est une donnée binaire.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY si la pièce jointe est un fichier.
    
   - ATTACH_EMBEDDED_MSG si la pièce jointe est un message.
    
   - ATTACH_OLE si la pièce jointe est un objet OLE.
    
3. Définissez la propriété de données de pièce jointe appropriée:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) pour les données binaires et les objets OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) pour les fichiers.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) pour les messages et les objets OLE 2.
    
4. Définissez **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) pour qu'il contienne la représentation graphique de la pièce jointe de fichier ou de pièces jointes binaires. Ne la définissez pas pour les objets OLE, qui stockent les informations de rendu en interne ou pour les messages attachés. 
    
5. Définissez **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) pour indiquer où la pièce jointe doit être affichée. **PR_RENDERING_POSITION** s'applique uniquement aux clients qui définissent la propriété **PR_BODY** . Si vous prenez en charge uniquement **PR_RTF_COMPRESSED**, placez les informations d'espace réservé suivantes dans le flux compressé:
    
   `\objattph`

   Pour définir **PR_RENDERING_POSITION**, affectez un nombre qui représente un décalage ordinal en caractères, le premier caractère de **PR_BODY** étant 0, si vous devez savoir où dans le message la pièce jointe est affichée, ou 0xFFFFFFFF, si vous ne le faites pas afficher les pièces jointes dans **PR_BODY**.
    
6. Définir **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) pour indiquer le nom abrégé du fichier pour un fichier joint et **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) pour indiquer le nom du fichier comme étant pris en charge sur une plateforme qui gère le format de nom de fichier long. Les deux propriétés sont facultatives. Toutefois, si vous définissez **PR_ATTACH_LONG_FILENAME**, définissez également **PR_ATTACH_FILENAME**. 
    
7. Définissez **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) pour indiquer le nom de la pièce jointe qui peut s'afficher dans une boîte de dialogue. PR_DISPLAY_NAME est facultatif. 
    
## <a name="set-prattachdatabin"></a>Définir PR_ATTACH_DATA_BIN
  
1. Appelez [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété avec l'interface **IStream** . 
    
2. Si un fichier contient les données et qu'il est ouvert ou si vous avez besoin d'un contrôle explicite sur la taille de la mémoire tampon, appelez **IStream:: Write** in a Loop to place the Data in the Stream. 
    
3. Une autre option consiste à appeler **OpenStreamOnFile** pour créer un flux pour accéder au fichier de données, puis appeler la méthode **IStream:: CopyTo** de ce flux pour copier les données dans le flux renvoyé par **OpenProperty**.
    
4. Appelez la méthode **IStream:: Commit** du nouveau flux. 
    
## <a name="set-prattachdataobj"></a>Définir PR_ATTACH_DATA_OBJ
  
1. Appelez **IMAPIProp:: OpenProperty** pour ouvrir la propriété avec l'interface **IStreamDocfile** afin de créer un flux qui fonctionne avec le stockage structuré. **IStreamDocfile** est implémenté par les fournisseurs de banques de messages pour permettre aux clients de stocker et de récupérer de manière plus efficace le stockage structuré. L'interface **IStreamDocfile** est identique à **IStream**, mais le contenu du flux est garanti être formaté en tant que stockage structuré. Si cet appel réussit, créez le flux en suivant les mêmes étapes que celles décrites pour le paramétrage de **PR_ATTACH_DATA_BIN**.
    
2. Si **OpenProperty** échoue: 
    
   1. Appelez à nouveau **OpenProperty** en demandant **IStorage**. 
      
   2. Appelez **StgOpenStorage** pour ouvrir l'objet OLE et renvoyer un objet de stockage. 
      
   3. Appelez la méthode **IStorage:: CopyTo** de l'objet de stockage renvoyé vers l'objet de stockage renvoyé à partir de **OpenProperty**.
      
   4. Appelez la méthode **IStorage:: Commit** de l'objet de stockage. 
    
## <a name="set-prattachpathname"></a>Définir PR_ATTACH_PATHNAME
  
1. AlLouez une structure [SPropValue](spropvalue.md) , en définissant le membre **ulPropTag** sur **PR_ATTACH_PATHNAME** et le membre **value. LPSZ** sur la chaîne de caractères qui représente le nom de fichier. 
    
2. Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de la pièce jointe. 
    
> [!NOTE]
> Si votre plateforme prend en charge les noms de fichier longs, définissez à la fois **PR_ATTACH_PATHNAME** et **PR_ATTACH_LONG_PATHNAME**. Il peut s'avérer nécessaire d'effectuer un appel de système d'exploitation pour récupérer le nom de fichier court. 
  
## <a name="see-also"></a>Voir aussi

- [Pièces jointes MAPI](mapi-attachments.md)

