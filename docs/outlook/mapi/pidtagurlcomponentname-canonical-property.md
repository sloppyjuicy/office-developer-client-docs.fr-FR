---
title: Propriété canonique PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: Nom du composant URL d’un message. Si elle n’est pas définie lors de la création du message, la magasin de messages doit définir ces propriétés en fonction de différentes propriétés de message.
ms.openlocfilehash: ab9ca3dee9c3e048f04b59bb2752aaa6afd1f679
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63741817"
---
# <a name="pidtagurlcomponentname-canonical-property"></a>Propriété canonique PidTagUrlComponentName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Nom du composant URL d’un message. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W  <br/> |
|Identificateur :  <br/> |0x10F3  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés doivent être uniques dans un dossier. Si elle n’est pas définie lors de la création du message, la magasin de messages doit définir ces propriétés en fonction de différentes propriétés de message, en fonction de la classe de message. Par exemple, **L’IPM. Remarque** et **IPM. Les** messages de rendez-vous doivent avoir cette propriété définie en fonction de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et de **l’IPM. Les** messages de contact doivent avoir cette propriété définie en fonction de la **propriété dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)). Pour la plupart des autres classes de message, cette propriété doit être basée sur la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
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

