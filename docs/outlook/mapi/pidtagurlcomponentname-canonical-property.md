---
title: Propriété canonique PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400333"
---
# <a name="pidtagurlcomponentname-canonical-property"></a>Propriété canonique PidTagUrlComponentName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le nom du composant URL pour un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W  <br/> |
|Identificateur :  <br/> |0x10F3  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés doivent être uniques au sein d’un dossier. Si ce n’est pas ensemble lorsque le message est créé, la banque de messages doit définir ces propriétés en fonction de diverses propriétés de message, en fonction de la classe de message. Par exemple, le **IPM. Note** et **IPM. Rendez-vous** messages doivent utilisent cette propriété en fonction de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et le **IPM. Contact** cette propriété doivent être définie en fonction de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) pour messages. Pour la plupart des autres classes de messages, cette propriété doit être basée sur la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
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

