---
title: Propriété canonique PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400256"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propriété canonique PidTagContainerClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de texte décrivant le type d’un dossier. Bien que cette propriété est ignorée en règle générale, cette propriété doit être présent prévoient des versions de Microsoft® Exchange Server avant de gestionnaire de boîte aux lettres Exchange Server 2003.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificateur :  <br/> |0x3613  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés ne sont pas normalement utilisées par Exchange Server. Toutefois, Microsoft Office Outlook® les attacher à des dossiers de boîte aux lettres. En outre, versions d’Exchange Server avant de gestionnaire de boîte aux lettres Exchange Server 2003 peuvent gérer correctement les dossiers qui n’ont pas ces propriétés.
  
Ces propriétés peuvent être attribuées les valeurs de chaîne dans le tableau suivant.
  
|**Valeur**|**Contenu du dossier**|
|:-----|:-----|
|ERREUR. Rendez-vous  <br/> |Rendez-vous  <br/> |
|ERREUR. Contact  <br/> |Contacts  <br/> |
|ERREUR. Journal  <br/> |Entrées de Journal Outlook  <br/> |
|ERREUR. Remarque  <br/> |Messages électroniques et des notes  <br/> |
|ERREUR. StickyNote  <br/> |Pense-bête Outlook  <br/> |
|ERREUR. Tâche  <br/> |Tâches Outlook  <br/> |
   
Pour les dossiers qui contiennent des messages électroniques, ces propriétés doivent être définies à l’erreur. Note.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les objets de liste de distribution personnelle.
    
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

