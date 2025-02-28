---
title: Propriété canonique PidTagMessageClass
description: Décrit la propriété canonique PidTagMessageClass, qui contient une chaîne de texte qui identifie la classe de message définie par l’expéditeur, telle que IPM. Note.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
ms.openlocfilehash: e8e19856f1671f403c3a27a41b13b09667e5c2d8
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752462"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propriété canonique PidTagMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de caractères qui identifie la classe de message définie par l’expéditeur, telle qu’une note IPM. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificateur :  <br/> |0x001A  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

La classe de message spécifie le type du message. Il détermine l’ensemble des propriétés définies pour le message, le type d’informations que le message transmet et la façon de gérer le message. 
  
Ces propriétés contiennent des chaînes concaténées avec des points. Chaque chaîne représente un niveau de sous-classe. Par exemple, IPM. Notez qu’il s’agit d’une sous-classe d’IPM et d’une superclasse d’IPM. Note.Private. 
  
Ces propriétés doivent se composer des caractères ASCII 32 à 127 et ne doivent pas se terminer par un point (ASCII 46). Les opérations de tri et de comparaison doivent la traiter comme une chaîne qui ne respecte pas la casse. La longueur maximale possible est de 255 caractères, mais pour permettre à la salle MAPI d’ajouter des qualificateurs, il est recommandé de conserver la longueur d’origine sous 128 caractères. 
  
Chaque message est nécessaire pour fournir ces propriétés. Normalement, l’application cliente qui crée un message le définit dès [qu’IMAPIFolder::CreateMessage](imapifolder-createmessage.md) est retourné avec succès. Toutefois, si la propriété n’a pas été définie lorsque le client appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md), le magasin de messages doit la définir sur IPM. 
  
Les valeurs définies par MAPI sont les suivantes : 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM et IPC sont destinés à être des superclasses uniquement, et un message doit avoir au moins un qualificateur de sous-classe ajouté avant d’être stocké ou envoyé. Pour plus d’informations sur l’utilisation de la classe de message, consultez [Classes de message](mapi-message-classes.md). Pour obtenir des listes de propriétés obligatoires et facultatives pour les classes de message, consultez les sous-rubriques [de About Message Properties](message-properties-overview.md).
  
Une classe de message personnalisée peut définir des propriétés dans une plage réservée à utiliser avec cette classe de message uniquement. Pour plus d’informations, consultez [À propos des identificateurs de propriétés](mapi-property-identifier-overview.md). 
  
Les classes de messages contrôlent le dossier de réception dans lequel un message entrant est stocké. Pour plus d’informations, consultez la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Pour plus d’informations sur l’utilisation de classes de message avec des formulaires et des serveurs de formulaires, consultez [Choisir une classe de message](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de courrier électronique.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour représenter les messages vocaux et de télécopie.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

