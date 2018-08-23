---
title: Propriété canonique PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: af5d05ee6d3592694952002c16e16188c3e458a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565619"
---
# <a name="pidtagattachtag-canonical-property"></a>Propriété canonique PidTagAttachTag

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’objet ASN.1 spécifiant l’application d'où provient d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_TAG  <br/> |
|Identificateur :  <br/> |0x370A  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie l’application qui a généré la pièce jointe.
  
 **Remarque** Les propriétés **PR_ATTACH_TAG** et **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) ne doivent pas être confondues. Ils ne sont pas couplés ou liées. **PR_ATTACH_ENCODING** identifie l’algorithme utilisé pour transformer les données dans une pièce jointe. « Objet » a une signification plus générale dans l’identificateur d’objet termes et l’utilisation X.400, que dans la programmation orientée objet. 
  
Les identificateurs d’objets objet identificateur la syntaxe et les exemples sont définies dans le MAPIOID. Fichier d’en-tête H. Valeurs de **PR_ATTACH_TAG** ne sont pas limités à ceux définis dans MAPIOID. H. 
  
Pour plus d’informations sur ces identificateurs d’objet, consultez la documentation sur ASN.1, X.208 et X.209. L’identificateur d’objet est trouvé dans l’élément de référence de l’application de l’environnement de fichier transférer corps composant FTBP (). 
  
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



[Propriété canonique PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

