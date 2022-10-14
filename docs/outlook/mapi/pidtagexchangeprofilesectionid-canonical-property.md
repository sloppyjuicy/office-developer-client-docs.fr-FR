---
title: Propriété canonique PidTagExchangeProfileSectionId
description: Décrit la propriété canonique PidTagExchangeProfileSectionId, qui contient un GUID généré dynamiquement.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
ms.openlocfilehash: 61d1a5a3b141a740d974cd6eef83bde7570ad6aa
ms.sourcegitcommit: b6d8fc4db483ecd1a3247a6cb3377f5b52c44cfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2022
ms.locfileid: "68574328"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propriété canonique PidTagExchangeProfileSectionId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un GUID généré dynamiquement utilisé pour déterminer un compte lorsque vous utilisez plusieurs comptes Microsoft Exchange Server.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificateur :  <br/> |0x3d150102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Comptes Exchange multiples  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Outlook 2010 et Microsoft Outlook 2013 prennent en charge plusieurs comptes Exchange au lieu d’un seul compte Exchange. Pour prendre en charge plusieurs comptes Exchange, la disposition du profil MAPI a été modifiée. Dans Microsoft Office Outlook 2007 et versions antérieures, les profils contenaient une section de profil fixe dédiée aux paramètres Exchange, comme le nom du serveur, le nom d’utilisateur et le fichier dossier hors connexion (.ost). Emplacement. Ces paramètres ont été identifiés à l’aide d’un identificateur unique, la propriété **pbGlobalProfileSectionGuid** . La section utilisée pour les paramètres Exchange est appelée section Profil global Exchange. 
  
Un emplacement de section de profil fixe n’est plus suffisant pour prendre en charge plusieurs comptes Exchange. Au lieu de cela, pour chaque compte Exchange de votre profil, il existe une section dédiée aux paramètres de ce compte. La nouvelle section utilisée pour les paramètres Exchange est identifiée par l’identificateur unique **emsmdbUID**.
  
Dans la section profil de service de message du compte Exchange, vous pouvez trouver une propriété qui contient un GUID généré dynamiquement au moment de la création du compte. Ce GUID est stocké dans la propriété **PidTagExchangeProfileSectionId** . Les magasins de messages et les conteneurs de carnets d’adresses exposent une propriété pour déterminer le compte Exchange auquel ils appartiennent. Accessible dans la table des services de messages, chaque service Exchange expose cette propriété. 
  
Vous pouvez récupérer cette propriété via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) sur **PidTagExchangeProfileSectionId** après avoir interrogé l’une des interfaces suivantes : 
  
- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Si l’objet n’est pas affilié à Exchange, l’appel retourne **MAPI_E_NOT_FOUND**.
  
Vous pouvez restreindre les conteneurs sur un **PidTagExchangeProfileSectionId** lors de l’affichage du carnet d’adresses. Une fois que vous disposez d’un conteneur ouvert, vous pouvez interroger **emsmdbUID** à partir de celui-ci. Il est également important de noter que si un destinataire a été sélectionné à partir d’un carnet d’adresses Exchange, le destinataire a également **pidTagExchangeProfileSectionId** dans sa liste de propriétés. 
  
> [!NOTE]
> Dans les exemples de code et les en-têtes de fonction, ce GUID est appelé **emsmdbUID**. 
  
L’un des comptes Exchange est marqué comme compte Exchange hérité. En règle générale, il s’agit du premier compte ajouté au profil. Chaque appel pour ouvrir **pbGlobalProfileSectionGuid** est redirigé vers la section globale Exchange du compte hérité. Les appels de modèle objet qui interagissent avec le compte Exchange non hérité interagissent également avec le compte Exchange hérité. 
  
Le service Exchange hérité a la propriété **PR_EMSMDB_LEGACY** (0x3D18000B), qui est définie sur **true** dans la table des services de messages. 
  
**L’emsmdbUID** hérité est également marqué dans la section Profil global Outlook du profil en tant que **PidTagExchangeProfileSectionId**. Le code écrit pour prendre en charge plusieurs comptes Exchange ne doit pas avoir à récupérer **l’emsmdbUID** hérité, car il doit obtenir **l’emsmdbUID** correct, en fonction du compte avec lequel votre code interagit.
  
## <a name="see-also"></a>Voir aussi



[Utilisation de plusieurs comptes Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](/training/paths/configure-user-device-profiles/)
