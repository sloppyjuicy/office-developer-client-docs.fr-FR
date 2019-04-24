---
title: Propriété canonique PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Dernière modification: 7 septembre 2016'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327257"
---
# <a name="pidtagattachmethod-canonical-property"></a>Propriété canonique PidTagAttachMethod

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une constante définie par MAPI qui représente le mode d'accès au contenu d'une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_METHOD  <br/> |
|Identificateur :  <br/> |0x3705  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l'une des valeurs suivantes:
  
NO_ATTACHMENT 
  
> La pièce jointe vient d'être créée. 
    
ATTACH_BY_VALUE 
  
> La propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contient les données de la pièce jointe. 
    
ATTACH_BY_REFERENCE 
  
> La propriété **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contient un chemin d'accès complet qui identifie la pièce jointe aux destinataires ayant accès à un fichier commun serveurs. 
    
ATTACH_BY_REF_RESOLVE 
  
> La propriété **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contient un chemin d'accès complet qui identifie la pièce jointe. 
    
ATTACH_BY_REF_ONLY 
  
> La propriété **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contient un chemin d'accès complet qui identifie la pièce jointe. 
    
ATTACH_EMBEDDED_MSG 
  
> La propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contient un objet incorporé qui prend en charge l'interface **IMessage** . 
    
ATTACH_OLE 
  
> La pièce jointe est un objet OLE incorporé.
    
ATTACH_BY_WEBREFERENCE 
  
> Le contenu de la pièce jointe n'est pas dans le message. 
    
Lors de sa création, tous les objets Attachment ont une valeur **PR_ATTACH_METHOD** initiale de **NO_ATTACHMENT**. 
  
Les applications clientes et les fournisseurs de services sont uniquement requis pour prendre en charge la méthode de pièce jointe représentée par la valeur **ATTACH_BY_VALUE** . Les autres méthodes de pièces jointes sont facultatives. La Banque de messages n'applique pas de cohérence entre la valeur de **PR_ATTACH_METHOD** et les valeurs des autres propriétés de pièces jointes. 
  
Les noms UNC (Universal Naming Convention) sont recommandés pour les chemins d'accès complets, qui doivent être utilisés avec **ATTACH_BY_REFERENCE** et **ATTACH_BY_REF_ONLY**. Avec **ATTACH_BY_REF_RESOLVE**, un chemin d'accès absolu est plus rapide, car le SPOULEur MAPI convertit la pièce jointe en **ATTACH_BY_VALUE**. 
  
Si **ATTACH_BY_REFERENCE** est défini, **PR_ATTACH_DATA_BIN** doit être vide. Une passerelle sortante peut transformer une pièce jointe **ATTACH_BY_REFERENCE** en une pièce jointe **ATTACH_BY_VALUE** en copiant les données de pièce jointe dans la propriété **PR_ATTACH_DATA_BIN** . 
  
Si **ATTACH_BY_REF_RESOLVE** est défini, **PR_ATTACH_DATA_BIN** doit être vide. Lorsque le message contenant la pièce jointe **ATTACH_BY_REF_RESOLVE** est envoyé, le spouleur MAPI copie les données de pièce jointe dans une pièce jointe **ATTACH_BY_VALUE** . Ce processus de résolution place les données des pièces jointes dans **PR_ATTACH_DATA_BIN**. 
  
Si **ATTACH_BY_REF_ONLY** est défini, **PR_ATTACH_DATA_BIN** doit être vide et le système de messagerie ne résout jamais la référence à la pièce jointe. Utilisez cette valeur lorsque vous souhaitez envoyer le lien, mais pas les données. 
  
Lorsque l'objet OLE est au format OLE 2,0 **IStorage** , les données sont accessibles via **PR_ATTACH_DATA_OBJ**. Lorsque l'objet OLE est au format OLE 1,0 **OLESTREAM** , les données sont accessibles via **PR_ATTACH_DATA_BIN** en tant qu' **IStream**. Le type d'encodage OLE peut être déterminé par la valeur de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Pour plus d'informations sur les interfaces et les formats OLE, consultez le *Guide de référence du programmeUr OLE* . 
  
## <a name="remarks"></a>Remarques

Lorsque le **PR_ATTACH_METHOD** est **ATTACH_BY_WEBREFERENCE**, le contenu de la pièce jointe n'est pas dans le message. Au lieu de cela, la propriété **PR_ATTACH_LONG_FILENAME** contient une URL absolue vers le contenu de la pièce jointe, qui est stocké en ligne. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

