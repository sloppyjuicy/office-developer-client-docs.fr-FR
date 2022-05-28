---
title: Propriété canonique PidTagContainerClass
description: Décrit la propriété canonique PidTagContainerClass, qui contient une chaîne de texte décrivant le type d’un dossier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
ms.openlocfilehash: 0d3709d97974002c4c2aa4383eca3bf214c98bd9
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769304"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Propriété canonique PidTagContainerClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de texte décrivant le type d’un dossier. Bien que cette propriété soit généralement ignorée, les versions de Microsoft® Exchange Server antérieures à Exchange Server 2003 Mailbox Manager s’attendent à ce que cette propriété soit présente.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Identificateur :  <br/> |0x3613  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Conteneur  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés ne sont normalement pas utilisées par Exchange Server. Toutefois, Microsoft Office Outlook ® les attache aux dossiers de boîte aux lettres. En outre, les versions de Exchange Server antérieures à Exchange Server Gestionnaire de boîtes aux lettres 2003 peuvent gérer de manière incorrecte les dossiers qui n’ont pas ces propriétés.
  
Ces propriétés peuvent être affectées aux valeurs de chaîne dans le tableau suivant.
  
|**Valeur**|**Contenu du dossier**|
|:-----|:-----|
|GIF. Nomination  <br/> |Rendez-vous  <br/> |
|GIF. Contact  <br/> |Contacts  <br/> |
|GIF. Journal  <br/> |entrées du journal Outlook  <br/> |
|GIF. Note  <br/> |Messages électroniques et notes  <br/> |
|GIF. StickyNote  <br/> |Outlook Pense-bêtes  <br/> |
|GIF. Tâche  <br/> |Tâches Outlook  <br/> |
   
Pour les dossiers contenant des messages électroniques, ces propriétés doivent être définies sur IPF. Note.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de liste de distribution de contacts et personnels.
    
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

