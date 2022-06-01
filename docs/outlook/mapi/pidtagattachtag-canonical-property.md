---
title: PidTagAttachTag Canonical, propriété
description: Décrit la propriété canonique PidTagAttachTag, qui contient un identificateur d’objet ASN.1 spécifiant l’application qui a fourni une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
ms.openlocfilehash: 4f6184e59ba6c0140373c713866926b04278746f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815281"
---
# <a name="pidtagattachtag-canonical-property"></a>PidTagAttachTag Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’objet ASN.1 spécifiant l’application qui a fourni une pièce jointe. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_TAG  <br/> |
|Identificateur :  <br/> |0x370A  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie l’application qui a généré la pièce jointe à l’origine.
  
 **Note** Les propriétés **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) et **PR_ATTACH_TAG** ne doivent pas être confondues. Ils ne sont pas associés ou associés. **PR_ATTACH_ENCODING** identifie l’algorithme utilisé pour transformer les données dans une pièce jointe. « Object » a une signification beaucoup plus générale dans l’identificateur d’objet de terme et dans l’utilisation de X.400, que dans la programmation orientée objet. 
  
La syntaxe de l’identificateur d’objet et les exemples d’identificateurs d’objet sont définis dans le MAPIOID. Fichier d’en-tête H. Les valeurs de **PR_ATTACH_TAG** ne sont pas limitées à celles définies dans MAPIOID.H. 
  
Pour obtenir des informations complètes sur ces identificateurs d’objet, consultez la documentation sur ASN.1, X.208 et X.209. L’identificateur d’objet se trouve dans l’élément de référence d’application de l’environnement FTBP (File Transfer Body Part). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

