---
title: Propriété canonique PidTagAttachTag
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 412c075ec414cf903125482dd83cf15f0307d909
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63719767"
---
# <a name="pidtagattachtag-canonical-property"></a>Propriété canonique PidTagAttachTag

  
  
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
  
 **Remarque** Les **propriétés PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) **et PR_ATTACH_TAG** ne doivent pas être confondues. Elles ne sont ni associées ni associées. **PR_ATTACH_ENCODING** identifie l’algorithme utilisé pour transformer les données dans une pièce jointe. « Object » a une signification beaucoup plus générale dans l’identificateur d’objet de terme et dans l’utilisation X.400 que dans la programmation orientée objet. 
  
La syntaxe de l’identificateur d’objet et les exemples d’identificateurs d’objet sont définis dans MAPIOID. Fichier d’en-tête H. Les **valeurs PR_ATTACH_TAG** ne sont pas limitées à celles définies dans MAPIOID.H. 
  
Pour plus d’informations sur ces identificateurs d’objets, voir la documentation sur ASN.1, X.208 et X.209. L’identificateur d’objet se trouve dans l’élément de référence d’application de l’environnement FTBP (File Transfer Body Part). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

