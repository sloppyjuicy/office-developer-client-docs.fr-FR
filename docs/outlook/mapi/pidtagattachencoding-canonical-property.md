---
title: Propriété canonique PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382770"
---
# <a name="pidtagattachencoding-canonical-property"></a>Propriété canonique PidTagAttachEncoding

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’objet ASN.1 qui spécifie le codage d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_ENCODING  <br/> |
|Identificateur :  <br/> |0x3702  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie l’algorithme utilisé pour transformer les données dans une pièce jointe.
  
 **Remarque** Les **PR_ATTACH_ENCODING** et les propriétés de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) ne doivent pas être confondues. Ils ne sont pas couplés ou liées. **PR_ATTACH_TAG** identifie l’application qui a généré la pièce jointe. « Objet » a une signification beaucoup plus générale X.400 et l’identificateur d’objet termes que dans la programmation orientée objet. 
  
Les identificateurs d’objets objet identificateur la syntaxe et les exemples sont définies dans le MAPIOID. Fichier d’en-tête H. Valeurs de **PR_ATTACH_ENCODING** ne sont pas limités à ceux définis dans MAPIOID. H. Par exemple, les fichiers Macintosh joints permet un identificateur tel que MacBinary. 
  
Pour plus d’informations sur ces identificateurs d’objet, consultez la documentation sur ASN.1, X.208 et X.209. L’identificateur d’objet est trouvé dans l’élément de référence de l’application de l’environnement FTBP (File Transfer Body Part). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

