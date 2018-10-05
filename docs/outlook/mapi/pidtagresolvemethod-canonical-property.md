---
title: Propriété canonique PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394901"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Propriété canonique PidTagResolveMethod

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur de résolution de conflit d’un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOLVE_METHOD  <br/> |
|Identificateur :  <br/> |0x3FE7  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété sur le dossier contenant le message de résolution de conflit indique comment résoudre le conflit. Cette propriété n’est pas requise. Toutefois, si elle est définie, indicateurs autres que les éléments suivants ne doivent pas être présents :
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0 X 00000000)  <br/> |Conflit de résoudre le message doit être généré.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0 X 00000001)  <br/> |Remplacer le message cible avec les dernières modifications seront appliquées.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0 X 00000002)  <br/> |Ne pas envoyer de message de notification de conflit lors de la génération de conflit de résoudre le message dans le dossier public.  <br/> |
   
Un client ou le serveur ne doit pas générer un message de résolution de conflit pour les messages associés. Ces messages doivent être résolus à l’aide de la sémantique **RESOLVE_METHOD_LAST_WRITER_WINS** . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de base de données qui sont utilisés dans les opérations à distance.
    
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

