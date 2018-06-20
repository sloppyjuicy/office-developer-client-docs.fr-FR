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
description: 'Dernière modification : 07 septembre 2016'
ms.openlocfilehash: 1720e9a2eeb54daed1e559f99b0c63ce09585419
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785742"
---
# <a name="pidtagattachmethod-canonical-property"></a>Propriété canonique PidTagAttachMethod

 
  
**S’applique à**: Outlook 
  
Contient une constante défini par MAPI représentant la façon dont le contenu d’une pièce jointe est accessible. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_METHOD  <br/> |
|Identificateur :  <br/> |0x3705  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement une des valeurs suivantes :
  
NO_ATTACHMENT 
  
> La pièce jointe vient d’être créée. 
    
ATTACH_BY_VALUE 
  
> La propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contient les données de pièce jointe. 
    
ATTACH_BY_REFERENCE 
  
> L' **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ou la propriété **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) contient un chemin d’accès complet qui identifie la pièce jointe aux destinataires d’accéder à un fichier commun serveur. 
    
ATTACH_BY_REF_RESOLVE 
  
> La propriété **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contient un chemin d’accès complet qui identifie la pièce jointe. 
    
ATTACH_BY_REF_ONLY 
  
> La propriété **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contient un chemin d’accès complet qui identifie la pièce jointe. 
    
ATTACH_EMBEDDED_MSG 
  
> La propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contient un objet incorporé qui prend en charge l’interface **IMessage** . 
    
ATTACH_OLE 
  
> La pièce jointe est un objet OLE incorporé.
    
ATTACH_BY_WEBREFERENCE 
  
> Le contenu de pièce jointe n’est pas dans le message. 
    
Une fois créée, tous les objets de pièces jointes ont une valeur initiale **PR_ATTACH_METHOD** **NO_ATTACHMENT**. 
  
Fournisseurs de services et les applications clientes sont uniquement requis pour prendre en charge la méthode de pièce jointe représentée par la valeur **ATTACH_BY_VALUE** . Les autres méthodes de pièce jointe sont facultatifs. La banque de messages n’applique pas la cohérence entre la valeur de **PR_ATTACH_METHOD** et les valeurs d’autres propriétés de la pièce jointe. 
  
Noms universal naming convention (UNC) sont recommandés pour les chemins complet, qui doivent être utilisées avec **ATTACH_BY_REFERENCE** et **ATTACH_BY_REF_ONLY**. Avec **ATTACH_BY_REF_RESOLVE**, un chemin d’accès absolu est plus rapide, car le spouleur MAPI convertit la pièce jointe **ATTACH_BY_VALUE**. 
  
Si **ATTACH_BY_REFERENCE** est défini, **PR_ATTACH_DATA_BIN** doit être vide. Une passerelle sortante peut activer une pièce jointe **ATTACH_BY_REFERENCE** dans une pièce jointe **ATTACH_BY_VALUE** en copiant des données de pièce jointe dans la propriété **PR_ATTACH_DATA_BIN** . 
  
Si **ATTACH_BY_REF_RESOLVE** est défini, **PR_ATTACH_DATA_BIN** doit être vide. Lorsque le message qui contient la pièce jointe **ATTACH_BY_REF_RESOLVE** est envoyé, le spouleur MAPI copie les données de pièce jointe dans une pièce jointe **ATTACH_BY_VALUE** . Ce processus de résolution place les données de pièce jointe dans **PR_ATTACH_DATA_BIN**. 
  
Si **ATTACH_BY_REF_ONLY** est défini, **PR_ATTACH_DATA_BIN** doit être vide, et le système de messagerie résout jamais la référence de la pièce jointe. Utilisez cette valeur lorsque vous souhaitez envoyer le lien, mais pas les données. 
  
Lorsque l’objet OLE est au format OLE 2.0 **IStorage** , les données sont accessibles via **PR_ATTACH_DATA_OBJ**. Lorsque l’objet OLE est au format OLE 1.0 **OLESTREAM** , les données sont accessibles via **PR_ATTACH_DATA_BIN** comme un **IStream**. Le type du codage OLE peut être déterminé par la valeur **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Pour plus d’informations sur les formats et les interfaces OLE, consultez la *référence du programmeur OLE* . 
  
## <a name="remarks"></a>Remarques

Une fois le **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE**, le contenu de pièce jointe n’est pas dans le message. Au lieu de cela, la propriété **PR_ATTACH_LONG_FILENAME** contient une URL absolue pour le contenu de pièce jointe, qui est stocké en ligne. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

