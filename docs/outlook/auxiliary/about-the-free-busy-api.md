---
title: À propos de l’API et de disponibilité
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: L’API de disponibilité permet de fournisseurs de messagerie fournir des informations de disponibilité pour les comptes d’utilisateur spécifié au sein d’une plage de temps spécifié.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782546"
---
# <a name="about-the-freebusy-api"></a>À propos de l’API et de disponibilité

L’API de disponibilité permet de fournisseurs de messagerie fournir des informations de disponibilité pour les comptes d’utilisateur spécifié au sein d’une plage de temps spécifié. L’état de disponibilité d’un bloc de temps sur le calendrier d’un utilisateur est une des opérations suivantes : hors du bureau, occupé (e), provisoire ou libre.
  
## <a name="create-a-freebusy-provider"></a>Créer un fournisseur et de disponibilité

Pour fournir des informations de disponibilité pour les utilisateurs de messagerie, un fournisseur de messagerie crée un fournisseur et de disponibilité et l’enregistre avec Outlook. Le fournisseur et de disponibilité doit implémenter les interfaces suivantes. Notez qu’un nombre de membres de ces interfaces n’est pas pris en charge et doit renvoyer que les valeurs de retour spécifié. En particulier, l’API de disponibilité ne gère pas un accès en écriture pour les informations de disponibilité et de déléguer l’accès aux comptes.
  
- [IFreeBusySupport](ifreebusysupport.md) — cette interface prend en charge la spécification des interfaces qui accèdent aux données de disponibilité pour les utilisateurs spécifiés. Il utilise [FBUser](fbuser.md) pour identifier un utilisateur. 
    
- [IFreeBusyData](ifreebusydata.md) — cette interface obtient et définit une plage de temps pour un utilisateur donné et retourne une interface pour énumérer les informations de disponibilité des blocs de données dans cette plage de temps. Il utilise une heure relative pour obtenir et définir ce laps de temps. Pour plus d’informations, voir [heure relative utilisés pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) — cette interface prend en charge l’accès et l’énumération des informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps. 
    
   > [!NOTE]
   > Une énumération contient des blocs de disponibilité qui indiquent l’état de disponibilité de périodes de temps dans le calendrier d’un utilisateur, au sein d’une plage de temps (spécifié par [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Éléments dans un calendrier, tels que des rendez-vous et des demandes de réunion, de blocs de forment dans l’énumération. Éléments à côté de l’autre dans le calendrier et ont le même statut de disponibilité sont combinées à former un bloc unique. Une période de temps dans un calendrier libre forms également un bloc. Par conséquent, aucune deux blocs consécutifs dans une énumération n’aurait le même état libre/occupé. Ces blocs ne se chevauchent pas dans le temps. Lorsqu’il existe des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour former des blocs de disponibilité sans chevauchement de l’énumération basée sur cet ordre de priorité : hors du bureau, provisoire, occupé (e). 
  
Pour enregistrer le fournisseur et de disponibilité avec Outlook, le fournisseur de messagerie doit procédez comme suit :
  
1. Enregistrez le fournisseur et de disponibilité avec COM, en fournissant un CLSID qui autorise l’accès à l’implémentation du fournisseur de **IFreeBusySupport**. 
    
2. Informer Outlook que le fournisseur et de disponibilité existe en définissant la clé suivante (où `<xx.x>` représente la version d’Outlook) dans le Registre système : 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Par exemple, si le fournisseur de transport est SMTP, pour enregistrer le fournisseur avec Microsoft Outlook 2010, définissez la clé suivante pour les données dans le tableau suivant : 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Name |Type |Valeur |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID d’implémentation respectif de IFreeBusySupport}  |
   
   Dans ce scénario, Outlook crée la classe COM et l’utilise pour récupérer des informations de disponibilité pour les utilisateurs de messagerie SMTP.
    
Pour prendre en charge un fournisseur de transport et le carnet d’adresses qui utilisent un type autre que SMTP entrée d’adresse, modifiez le *nom* en conséquence. 
  
> [!NOTE]
> Pendant l’installation, les fournisseurs et de disponibilité doivent vérifier si un paramètre de Registre pour le même type entrée existe déjà. Si c’est le cas, le fournisseur et de disponibilité doit remplacer le fournisseur en cours pour ce type de l’entrée d’adresse et restaurer à ce fournisseur lors de la désinstallation. Toutefois, si un utilisateur a installé plusieurs fournisseurs et de disponibilité pour le même type de l’entrée d’adresse, l’utilisateur doit désinstaller ces fournisseurs dans l’ordre inverse en tant que l’installation (autrement dit, désinstallez toujours le fournisseur le plus récent). Dans le cas contraire, le Registre peut pointer vers un fournisseur qui a déjà été désinstallé. 
  
## <a name="api-components"></a>Composants de l’API

L’API de disponibilité comprend les composants suivants :
  
### <a name="definitions"></a>Définitions

- [Constantes (disponibilité API)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Types de données

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

