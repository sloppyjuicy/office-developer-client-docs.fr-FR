---
title: Propriété canonique PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699512"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propriété canonique PidTagExchangeProfileSectionId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un GUID généré de manière dynamique permet de déterminer un compte lorsque vous utilisez plusieurs comptes Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificateur :  <br/> |0x3d150102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Comptes Exchange multiples  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Outlook 2010 et Microsoft Outlook 2013 prend en charge plusieurs comptes Exchange au lieu d’un seul compte Exchange. Pour prendre en charge plusieurs comptes Exchange, la mise en page de profil MAPI a été modifié. Dans Microsoft Office Outlook 2007 et versions antérieures, profils contenu dans une section de profil fixe dédiée aux paramètres Exchange comme nom du serveur, nom d’utilisateur et le fichier de dossier en mode hors connexion (.ost). emplacement. Ces paramètres ont été identifiés à l’aide d’un identificateur unique de la propriété **pbGlobalProfileSectionGuid** . La section utilisée pour les paramètres Exchange est appelée la Section globale Exchange. 
  
Un emplacement de la section profil fixe n’est plus suffisant pour prendre en charge plusieurs comptes Exchange. Au lieu de cela, pour chaque compte Exchange dans votre profil, il existe une section consacrée aux paramètres de ce compte. La nouvelle section utilisée pour les paramètres Exchange est identifiée par l' identificateur unique **emsmdbUID**.
  
Dans la section de profil de service de message pour le compte Exchange, vous pouvez trouver une propriété qui contient un GUID qui est généré de manière dynamique au moment où le compte est créé. Ce GUID est stocké dans la propriété **PidTagExchangeProfileSectionId** . Banques de messages et les conteneurs de carnet d’adresses exposent une propriété pour déterminer quel compte Exchange auxquels ils appartiennent. Accessibles dans le tableau des services message, chaque service Exchange expose cette propriété. 
  
Vous pouvez extraire cette propriété via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) sur **PidTagExchangeProfileSectionId** après interrogation pour une des interfaces suivantes : 
  
- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Si l’objet n’est pas affilié Exchange, l’appel renvoie **MAPI_E_NOT_FOUND**.
  
Vous pouvez restreindre les conteneurs sur un **PidTagExchangeProfileSectionId** lors de l’affichage du carnet d’adresses. Une fois que vous avez un conteneur ouvert, vous pouvez interroger l' **emsmdbUID** à partir de celui-ci. Il est également important de noter que si un destinataire a été sélectionné dans un carnet d’adresses de Exchange, le destinataire a également la **PidTagExchangeProfileSectionId** dans sa liste des propriétés. 
  
> [!NOTE]
> Dans les exemples de code et les en-têtes de fonction, ce GUID est appelé **emsmdbUID**. 
  
Un des comptes Exchange est marqué comme le compte Exchange hérité. En règle générale, il est le premier compte ajouté au profil. Chaque appel pour ouvrir **pbGlobalProfileSectionGuid** est redirigé vers la section globale Exchange du compte hérité. Les appels de modèle objet qui interagissent avec un compte Exchange non héritée également interagissent avec le compte Exchange hérité. 
  
Le service Exchange hérité possède la propriété **PR_EMSMDB_LEGACY** (0x3D18000B), qui est défini sur **true** dans la table des services. 
  
Les anciens **emsmdbUID** est également marqué dans la Section de profil Outlook globale du profil en tant que **PidTagExchangeProfileSectionId**. Le code écrit pour prendre en charge plusieurs comptes Exchange devront pas récupérer les anciens **emsmdbUID** , car il doit obtenir le correct **emsmdbUID**, selon le compte d’avec que votre code interagit.
  
## <a name="see-also"></a>Voir aussi



[Utilisation de plusieurs comptes Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

