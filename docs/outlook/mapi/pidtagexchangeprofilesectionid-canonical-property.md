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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316428"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propriété canonique PidTagExchangeProfileSectionId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un GUID généré dynamiquement utilisé pour déterminer un compte lorsque vous utilisez plusieurs comptes Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificateur :  <br/> |0x3D150102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Comptes Exchange multiples  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Outlook 2010 et Microsoft Outlook 2013 prennent en charge plusieurs comptes Exchange au lieu d'un seul compte Exchange. Pour prendre en charge plusieurs comptes Exchange, la disposition du profil MAPI a été modifiée. Dans Microsoft Office Outlook 2007 et versions antérieures, les profils contiennent une section de profil fixe dédiée aux paramètres Exchange, tels que le nom du serveur, le nom d'utilisateur et le fichier de dossiers en mode hors connexion (. ost). emplacements. Ces paramètres ont été identifiés à l'aide d'un identificateur unique, la propriété **pbGlobalProfileSectionGuid** . La section utilisée pour les paramètres Exchange est appelée la section profil global Exchange. 
  
Un emplacement de section de profil fixe n'est plus suffisant pour prendre en charge plusieurs comptes Exchange. Au lieu de cela, pour chaque compte Exchange de votre profil, il existe une section dédiée aux paramètres de ce compte. La nouvelle section utilisée pour les paramètres Exchange est identifiée par l'identificateur unique **emsmdbUID**.
  
Dans la section profil de service de messagerie du compte Exchange, vous pouvez rechercher une propriété qui contient un GUID généré dynamiquement lors de la création du compte. Ce GUID est stocké dans la propriété **PidTagExchangeProfileSectionId** . Les banques de messages et les conteneurs du carnet d'adresses exposent une propriété pour déterminer le compte Exchange auquel elle appartient. Accessible dans le tableau des services de messagerie, chaque service Exchange expose cette propriété. 
  
Vous pouvez récupérer cette propriété via un appel à [IMAPIProp:: GetProps](imapiprop-getprops.md) sur **PidTagExchangeProfileSectionId** après avoir effectué une requête pour l'une des interfaces suivantes: 
  
- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Si l'objet n'est pas affilié à Exchange, l'appel renvoie **MAPI_E_NOT_FOUND**.
  
Vous pouvez limiter les conteneurs sur un **PidTagExchangeProfileSectionId** lors de l'affichage du carnet d'adresses. Une fois que vous avez ouvert un conteneur, vous pouvez interroger le **emsmdbUID** à partir de celui-ci. Notez également que si un destinataire a été sélectionné dans un carnet d'adresses Exchange, le destinataire a également le **PidTagExchangeProfileSectionId** dans sa liste de propriétés. 
  
> [!NOTE]
> Tout au long des exemples de code et des en-têtes de fonction, ce GUID est appelé **emsmdbUID**. 
  
L'un des comptes Exchange est marqué comme compte Exchange hérité. En règle générale, il s'agit du premier compte ajouté au profil. Chaque appel à Open **pbGlobalProfileSectionGuid** est redirigé vers la section Exchange global du compte hérité. Les appels de modèle objet qui interagissent avec le compte Exchange non hérité interagissent également avec le compte Exchange hérité. 
  
Le service Exchange hérité a la propriété **PR_EMSMDB_LEGACY** (0x3D18000B), qui est définie sur **true** dans le tableau des services de messagerie. 
  
La **emsmdbUID** héritée est également marquée dans la section de profil global Outlook du profil en tant que **PidTagExchangeProfileSectionId**. Le code écrit pour prendre en charge plusieurs comptes Exchange ne doit pas avoir à récupérer le **emsmdbUID** hérité, car il doit obtenir le **emsmdbUID**correct, en fonction du compte avec lequel votre code interagit.
  
## <a name="see-also"></a>Voir aussi



[Utilisation de plusieurs comptes Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

