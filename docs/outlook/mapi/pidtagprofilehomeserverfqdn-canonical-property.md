---
title: Propriété canonique PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b02a55f7b87bef6a4304d006f79472bcf21c811e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581873"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Propriété canonique PidTagProfileHomeServerFQDN

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Active l’authentification Kerberos d’une configuration de profil.
  
****

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Identificateur :  <br/> |0x662A001F  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Configuration d’un profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Définir cette propriété sur le nom de domaine du serveur d’annuaire de l’utilisateur permet à connexion directe pour le contrôleur de domaine (DC), qui est nécessaire pour un profil a été configuré pour utiliser l’authentification Kerberos par rapport à Microsoft Exchange Server 2007 et versions antérieures, en définissant **RPC_C_AUTHN_GSS_KERBEROS** dans **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 et Exchange Server 2013 gérer les appels de carnet d’adresse apportées au serveur d’accès Client différent de celui dans lequel Exchange Server 2007 et versions antérieures les gérer. Le processus DSProxy n’est plus utilisé, afin que l’authentification Kerberos peut s’exécuter correctement. Toutefois, le client doit toujours communiquer avec le serveur Exchange, plutôt que directement avec le contrôleur de domaine ne peut pas être souhaitée : paramètre **PR_PROFILE_HOME_SERVER_FQDN** permet de l’éviter. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Spécifie les opérations autorisées pour les objets de banque de messages principale.
    
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

