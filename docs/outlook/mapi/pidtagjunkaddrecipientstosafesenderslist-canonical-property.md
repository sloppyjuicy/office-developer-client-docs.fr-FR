---
title: Propriété canonique PidTagJunkAddRecipientsToSafeSendersList
description: Décrit la propriété canonique PidTagJunkAddRecipientsToSafeSendersList, qui indique si les destinataires de courrier doivent être ajoutés à la liste des expéditeurs approuvés.
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
ms.openlocfilehash: 141dc6d67e806ab7ccf74f69307fb89e4e412510
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752588"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Propriété canonique PidTagJunkAddRecipientsToSafeSendersList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si les destinataires de courrier doivent être ajoutés ou non à la liste des expéditeurs approuvés.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Identificateur :  <br/> |0x6103  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est présente, cette propriété doit être définie sur 0 ou 1. La valeur 1 indique que les destinataires de courrier doivent être ajoutés à la liste des expéditeurs approuvés. La valeur 0 indique que les destinataires de courrier ne doivent pas être ajoutés à la liste des expéditeurs approuvés.
  
Si cette propriété est présente avec la valeur 1, les adresses SMTP des destinataires de l’e-mail doivent être ajoutées à la clause expéditeurs approuvés de la condition de règle de courrier indésirable. Si cette propriété a la valeur 0, aucune action n’est requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’autorisation/de blocage et la détermination des courriers indésirables.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

