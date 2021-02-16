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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283148"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propriété canonique PidTagContainerClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de texte décrivant le type d’un dossier. Bien que cette propriété soit généralement ignorée, les versions de Microsoft® Exchange Server antérieures à Exchange Server 2003 Mailbox Manager s’attendent à ce que cette propriété soit présente.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificateur :  <br/> |0x3613  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés ne sont normalement pas utilisées par les Exchange Server. Toutefois, Microsoft Office Outlook® les joint à des dossiers de boîte aux lettres. En outre, les versions de Exchange Server antérieures à Exchange Server 2003 Mailbox Manager peuvent gérer de manière incorrecte les dossiers qui n’ont pas ces propriétés.
  
Ces propriétés peuvent être affectées aux valeurs de chaîne dans le tableau suivant.
  
|**Valeur**|**Contenu du dossier**|
|:-----|:-----|
|IPF. Rendez-vous  <br/> |Rendez-vous  <br/> |
|IPF. Contact  <br/> |Contacts  <br/> |
|IPF. Journal  <br/> |Entrées du journal Outlook  <br/> |
|IPF. Remarque  <br/> |Messages électroniques et notes  <br/> |
|IPF. StickyNote  <br/> |Outlook Sticky Notes  <br/> |
|IPF. Tâche  <br/> |Tâches Outlook  <br/> |
   
Pour les dossiers qui contiennent des messages électroniques, ces propriétés doivent être définies sur IPF. Remarque.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de liste de distribution personnelle et de contact.
    
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

