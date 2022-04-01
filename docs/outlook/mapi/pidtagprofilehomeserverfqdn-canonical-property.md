---
title: Propriété canonique PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: Active l’authentification Kerberos d’une configuration de profil. La définition de cette propriété sur le nom de domaine du serveur d’annuaire de l’utilisateur permet une connexion directe au contrôleur de domaine.
ms.openlocfilehash: 51f2f620f2f3ecad23d307f79273ecbf88af6b26
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523489"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Propriété canonique PidTagProfileHomeServerFQDN

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active l’authentification Kerberos d’une configuration de profil.
  
****

|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Identificateur :  <br/> |0x662A001F  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Configuration de profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La définition de cette propriété sur le nom de domaine du serveur d’annuaire de l’utilisateur permet une connexion directe au contrôleur de domaine (DC), ce qui est nécessaire pour un profil configuré pour utiliser l’authentification Kerberos par rapport à Microsoft Exchange Server 2007 et versions antérieures, en configurant **RPC_C_AUTHN_GSS_KERBEROS** dans **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 et Exchange Server 2013 gèrent les appels de carnet d’adresses effectués vers le serveur d’accès au client différemment de la manière dont Exchange Server 2007 et les versions antérieures les gèrent. Le processus DSProxy n’est plus utilisé, donc l’authentification Kerberos peut réussir. Toutefois, le client communiquerait toujours avec le serveur Exchange au lieu de communiquer directement avec le dc, ce qui n’est peut-être pas souhaité : la  définition de PR_PROFILE_HOME_SERVER_FQDN évite cela. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Spécifie les opérations autorisées pour les objets principaux de la boutique de messages.
    
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

