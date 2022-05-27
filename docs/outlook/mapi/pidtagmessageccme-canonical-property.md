---
title: Propriété canonique PidTagMessageCcMe
description: Décrit la propriété canonique PidTagMessageCcMe, qui est un moyen pratique de déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires CC.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
ms.openlocfilehash: 46e825f499ffebc08c3173de9499014f055969bf
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752742"
---
# <a name="pidtagmessageccme-canonical-property"></a>Propriété canonique PidTagMessageCcMe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si cet utilisateur de messagerie est spécifiquement nommé en tant que destinataire de copie carbone (CC) de ce message et ne fait pas partie d’une liste de distribution. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Identificateur :  <br/> |0x0058  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un moyen pratique de déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires de copie carbone, sans examiner toutes les entrées de la liste. 
  
Cette propriété facilite également la gestion automatisée des messages reçus au moment de la réception. À l’option du fournisseur de transport, cette propriété contient FALSE ou n’est pas définie si l’utilisateur de messagerie n’est pas répertorié directement dans la table des destinataires. 
  
La remise des messages résultant de l’expansion de la liste de distribution ou d’une désignation de copie carbone aveugle n’entraîne pas la définition de cette propriété. Le destinataire doit être nommé explicitement. 
  
Les messages non envoyés ne définissent généralement pas cette propriété, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). S’ils sont présents dans les messages auxquels l’utilisateur peut accéder dans les magasins de messages publics, dans les magasins privés d’autres utilisateurs, dans les fichiers sur disque ou incorporés dans d’autres messages reçus, ils contiennent généralement les valeurs auxquelles ils ont été définis la dernière fois qu’un fournisseur de transport a remis le message. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées sur les objets de courrier électronique.
    
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

