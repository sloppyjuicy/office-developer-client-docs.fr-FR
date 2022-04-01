---
title: Propriété canonique PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5c9520595e1bacafb5e4ddd4920f82021e3ba0ee
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523774"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Propriété canonique PidTagJunkAddRecipientsToSafeSendersList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si les destinataires de messagerie doivent être ajoutés à la liste des expéditeurs sûrs.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Identificateur :  <br/> |0x6103  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est présente, cette propriété doit être définie sur 0 ou 1. La valeur 1 indique que les destinataires de courrier doivent être ajoutés à la liste des expéditeurs sûrs. La valeur 0 indique que les destinataires de courrier ne doivent pas être ajoutés à la liste des expéditeurs sûrs.
  
Si cette propriété est présente avec la valeur 1, les adresses SMTP des destinataires du courrier électronique doivent être ajoutées à la clause des expéditeurs fiables de la condition de règle de courrier indésirable. Si cette propriété a la valeur 0, aucune action n’est requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’adresses de courriers indésirables et la détermination des messages électroniques indésirables.
    
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

