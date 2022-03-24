---
title: Propriété canonique PidTagExchangeProfileSectionId
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2593d1c7292e393cd2b2f62526b33a18de6592c1
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724546"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propriété canonique PidTagExchangeProfileSectionId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un GUID généré dynamiquement utilisé pour déterminer un compte lorsque vous utilisez plusieurs Microsoft Exchange Server comptes.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificateur :  <br/> |0x3d150102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Comptes Exchange multiples  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Outlook 2010 et Microsoft Outlook 2013 prendre en charge plusieurs comptes Exchange au lieu d’un seul compte Exchange unique. Pour prendre en charge plusieurs Exchange, la disposition du profil MAPI a été modifiée. Dans Microsoft Office Outlook 2007 et les précédentes, les profils contenaient une section de profil fixe dédiée aux paramètres Exchange tels que le nom du serveur, le nom d’utilisateur et le fichier de dossier hors connexion (.ost). emplacement. Ces paramètres ont été identifiés à l’aide d’un identificateur unique, la **propriété pbGlobalProfileSectionGuid** . La section utilisée pour Exchange paramètres est appelée section Exchange de profil global. 
  
Un emplacement de section de profil fixe ne suffit plus pour prendre en charge plusieurs Exchange comptes. Au lieu de cela, pour chaque Exchange de votre profil, il existe une section dédiée aux paramètres de ce compte. La nouvelle section utilisée pour Exchange paramètres est identifiée par **l’identificateur unique emsmdbUID**.
  
Dans la section profil de service de message pour le compte Exchange, vous pouvez trouver une propriété qui contient un GUID qui est généré dynamiquement au moment de la création du compte. Ce GUID est stocké dans la **propriété PidTagExchangeProfileSectionId** . Les magasins de messages et les conteneurs de carnet d’adresses exposent une propriété pour déterminer Exchange compte auquel ils appartiennent. Accessible dans la table des services de messages, chaque service Exchange expose cette propriété. 
  
Vous pouvez récupérer cette propriété via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) sur **PidTagExchangeProfileSectionId** après avoir fait une requête pour l’une des interfaces suivantes : 
  
- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Si l’objet n’est pas Exchange, l’appel renvoie **MAPI_E_NOT_FOUND**.
  
Vous pouvez restreindre les conteneurs sur **un pidTagExchangeProfileSectionId** lors de l’affichage du carnet d’adresses. Une fois que vous avez un conteneur ouvert, vous pouvez interroger **emsmdbUID à** partir de celui-ci. Il est également intéressant de noter que si un destinataire a été sélectionné dans un carnet d’adresses Exchange, le destinataire possède également le **PidTagExchangeProfileSectionId** dans sa liste de propriétés. 
  
> [!NOTE]
> Tout au long des exemples de code et des en-têtes de fonction, ce GUID est appelé **emsmdbUID**. 
  
L’un des Exchange est marqué comme compte Exchange hérité. En règle générale, il s’agit du premier compte ajouté au profil. Chaque appel pour **ouvrir pbGlobalProfileSectionGuid** est redirigé vers la section Exchange globale du compte hérité. Les appels de modèle objet qui interagissent avec le compte Exchange non hérité interagissent également avec le compte Exchange hérité. 
  
Le service Exchange hérité possède la propriété **PR_EMSMDB_LEGACY** (0x3D18000B), qui est définie sur **true** dans la table des services de messages. 
  
**L’emsmdbUID** hérité est également marqué dans la section Outlook Profil global du profil en tant que **PidTagExchangeProfileSectionId**. Le code écrit pour prendre en charge plusieurs comptes Exchange ne doit pas avoir à récupérer **l’emsmdbUID** hérité, car il doit obtenir le **emsmdbUID** correct, en fonction du compte avec qui votre code interagit.
  
## <a name="see-also"></a>Voir aussi



[Utilisation de comptes Exchange multiples](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

