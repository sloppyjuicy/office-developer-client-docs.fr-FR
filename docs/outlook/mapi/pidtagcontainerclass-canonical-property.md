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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283148"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propriété canonique PidTagContainerClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de texte décrivant le type d'un dossier. Bien que cette propriété soit généralement ignorée, les versions de Microsoft ® Exchange Server antérieures à Exchange Server 2003 gestionnaire de boîtes aux lettres s'attendent à ce que cette propriété soit présente.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificateur :  <br/> |0x3613  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés ne sont pas normalement utilisées par Exchange Server. Toutefois, Microsoft Office Outlook ® les joint à des dossiers de boîte aux lettres. En outre, les versions d'Exchange Server antérieures à Exchange Server 2003 Mailbox Manager peuvent gérer de manière incorrecte les dossiers qui ne possèdent pas ces propriétés.
  
Ces propriétés peuvent être assignées aux valeurs de chaîne dans le tableau suivant.
  
|**Valeur**|**Contenu du dossier**|
|:-----|:-----|
|Page. Rendez-vous  <br/> |Rendez-vous  <br/> |
|Page. Prenez  <br/> |Contacts  <br/> |
|Page. N  <br/> |Entrées du journal Outlook  <br/> |
|Page. Note  <br/> |Messages électroniques et notes  <br/> |
|Page. StickyNote  <br/> |Pense-bête Outlook  <br/> |
|Page. Tâche  <br/> |Tâches Outlook  <br/> |
   
Pour les dossiers qui contiennent des messages électroniques, ces propriétés doivent être définies sur IPF. Note.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de liste de distribution personnelle et de contact.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

