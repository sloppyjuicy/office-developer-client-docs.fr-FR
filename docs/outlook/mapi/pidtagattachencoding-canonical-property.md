---
title: Propriété canonique PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9716af43b65b8bbc9b1d2c3b8b0b3d549b635afd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583582"
---
# <a name="pidtagattachencoding-canonical-property"></a>Propriété canonique PidTagAttachEncoding

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’objet ASN.1 qui spécifie le codage d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_ENCODING  <br/> |
|Identificateur :  <br/> |0x3702  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie l’algorithme utilisé pour transformer les données dans une pièce jointe.
  
 **Remarque** Les **propriétés PR_ATTACH_ENCODING** et **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) ne doivent pas être confondues. Elles ne sont ni associées ni associées. **PR_ATTACH_TAG** identifie l’application qui a généré la pièce jointe à l’origine. « Object » a une signification beaucoup plus générale dans l’identificateur d’objet de terme et dans X.400 que dans la programmation orientée objet. 
  
La syntaxe de l’identificateur d’objet et les exemples d’identificateurs d’objet sont définis dans MAPIOID. Fichier d’en-tête H. Les **valeurs PR_ATTACH_ENCODING** ne sont pas limitées à celles définies dans MAPIOID.H. Par exemple, les fichiers Macintosh joints peuvent utiliser un identificateur tel que MacBinary. 
  
Pour plus d’informations sur ces identificateurs d’objets, voir la documentation sur ASN.1, X.208 et X.209. L’identificateur d’objet se trouve dans l’élément de référence d’application de l’environnement FTBP (File Transfer Body Part). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

