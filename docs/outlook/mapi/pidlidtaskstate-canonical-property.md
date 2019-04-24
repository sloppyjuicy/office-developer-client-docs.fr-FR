---
title: Propriété canonique PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316533"
---
# <a name="pidlidtaskstate-canonical-property"></a>Propriété canonique PidLidTaskState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l'état d'affectation actuel de la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskState  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Task  <br/> |
|ID long (couvercle):  <br/> |0x00008113  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être l'une des valeurs suivantes.
  
|**Value**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Cette tâche a été créée pour correspondre à une tâche qui a été incorporée dans un rejet de tâche mais qui n'a pas pu être trouvée localement.  <br/> |
|0x00000001  <br/> |La tâche n'est pas affectée.  <br/> |
|0x00000002  <br/> |La tâche est la copie de la tâche affectée par le destinataire de la tâche.  <br/> |
|0x00000003  <br/> |La tâche est la copie de la tâche affectée de la tâche.  <br/> |
|0x00000004  <br/> |La tâche est la copie de la tâche rejetée de l'asserteur de tâche.  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l'ordre et le flux de transfert de données entre un client et un serveur.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

