---
title: Propriété canonique PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 30482f7d6acef7377a1b63bc3de4e43be48d8608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583357"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Propriété canonique PidTagDisplayTypeEx

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le type d’une entrée, en ce qui concerne l’entrée affichage sur une ligne dans une table de la liste d’adresses globale. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Identificateur :  <br/> |0x3905  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie le type d’une entrée, en ce qui concerne comment il doit être affiché dans la liste d’adresses globale. Il fournit des informations supplémentaires qui ne peut pas être représentées dans **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Les valeurs de cette propriété et **PR_DISPLAY_TYPE** commencent par « Du préfixeDT_ » et sont définies dans Mapitags.h. Toutes les valeurs non documentées sont réservés pour MAPI. Applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêts à traiter avec une valeur non documentée. 
  
Il existe certaines macros qui peuvent aider à déterminer les attributs d’un objet tel qu’il s’agisse local, à distance ou sécurisé. Ces macros sont les suivants : 
  
|**Macro**|**Valeur**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0 x 80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0 x 40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0 X 00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0 X 00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0 X 00000009)  <br/> |
   
Voici quelques conseils sur l’utilisation de ces macros. 
  
- Pour vérifier si une entrée est une entrée dans une autre forêt distante, appliquer la macro DTE_IS_REMOTE_VALID à la valeur de cette propriété pour vérifier si l’indicateur DTE_FLAG_REMOTE_VALID est défini dans l’entrée. S’il s’agit d’une entrée à distance, vous pouvez puis déterminer le type de l’entrée à distance à l’aide de la macro DTE_REMOTE. 
    
- Dans les configurations de forêt unique et de plusieurs forêts, lorsque **PR_DISPLAY_TYPE** a la valeur de DT_DISTLIST et DTE_IS_REMOTE_VALID a la valeur false, l’application de la macro DTE_LOCAL à la valeur de cette propriété peut vous permettre de mieux identifier le type de l’objet en tant que DT_DISTLIST (une liste de distribution) ou DT_SEC_DISTLIST (une liste de distribution de sécurité). 
    
- Si vous appliquez la macro DTE_LOCAL à la valeur de **PR_DISPLAY_TYPE_EX** , et elle renvoie le type DT_REMOTE_MAILUSER, l’entrée est une entrée à distance. 
    
- Dans une seule forêt ou dans une configuration de plusieurs forêts où la réplication est contrôlée par une liste de contrôle d’accès (ACL), vous pouvez utiliser la macro DTE_IS_ACL_CAPABLE pour déterminer si une entrée est une entité de sécurité.
    
Dans une configuration de plusieurs forêts, **PR_DISPLAY_TYPE** a la valeur DT_REMOTE_MAILUSER. Application de la macro DTE_REMOTE à la valeur de cette propriété peut vous permettre d’obtenir le type de l’entrée à distance. Les types possibles d’entrée à distance sont les suivantes : 
  
|**Type d’entrée à distance**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0 X 00000003)  <br/> |Liste de distribution dynamique.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0 X 00000001)  <br/> |Liste de distribution.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0 X 00000008)  <br/> |Équipement, par exemple, une imprimante ou un projecteur.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0 X 00000000)  <br/> |Utilisateur disposant d’une boîte aux lettres.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0 X 00000000)  <br/> |Une entrée de liste d’adresses dans la liste d’adresses globale.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0 X 00000007)  <br/> |Salle de conférence.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0 X 00000009)  <br/> |Liste de distribution de sécurité.  <br/> |
   
Dans une seule forêt et dans plusieurs forêts configuration, lorsque **PR_DISPLAY_TYPE** a la valeur de DT_DISTLIST et DTE_IS_REMOTE_VALID a la valeur false, l’application de la macro DTE_LOCAL à la valeur de cette propriété peut vous permettre d’obtenir le type de la liste de distribution . Les types de liste de distribution possibles sont les suivantes : 
  
|**Type de liste de Distribution**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0 X 00000001)  <br/> |Liste de distribution.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0 X 00000009)  <br/> |Liste de distribution de sécurité.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
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

