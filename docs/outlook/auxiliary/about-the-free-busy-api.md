---
title: À propos de l’API Disponibilité
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: L'API de disponibilité permet aux fournisseurs de messagerie de fournir des informations de disponibilité pour les comptes d'utilisateurs spécifiés dans un intervalle de temps spécifié.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317009"
---
# <a name="about-the-freebusy-api"></a>À propos de l’API Disponibilité

L'API de disponibilité permet aux fournisseurs de messagerie de fournir des informations de disponibilité pour les comptes d'utilisateurs spécifiés dans un intervalle de temps spécifié. L'état de disponibilité d'une plage de temps sur le calendrier d'un utilisateur est l'un des suivants: absent (e) du bureau, inactif, provisoire ou gratuit.
  
## <a name="create-a-freebusy-provider"></a>Créer un fournisseur de disponibilité

Pour fournir des informations de disponibilité aux utilisateurs de messagerie, un fournisseur de messagerie crée un fournisseur de disponibilité et l'enregistre auprès d'Outlook. Le fournisseur de disponibilité doit implémenter les interfaces suivantes. Notez qu'un certain nombre de membres dans ces interfaces ne sont pas pris en charge et doivent renvoyer les valeurs renvoyées spécifiées. En particulier, l'API de disponibilité ne prend pas en charge l'accès en écriture aux informations de disponibilité et l'accès délégué aux comptes.
  
- [IFreeBusySupport](ifreebusysupport.md) : cette interface prend en charge la spécification des interfaces qui accèdent aux données de disponibilité pour les utilisateurs spécifiés. Il utilise [FBUser](fbuser.md) pour identifier un utilisateur. 
    
- [IFreeBusyData](ifreebusydata.md) : cette interface obtient et définit une plage horaire pour un utilisateur donné et retourne une interface pour l'énumération des blocs de données de disponibilité dans cette plage de temps. Il utilise l'heure relative pour obtenir et définir ce intervalle de temps. Pour plus d'informations, consultez la rubrique [utilisation de l'heure relative pour accéder aux données de](how-to-use-relative-time-to-access-free-busy-data.md)disponibilité.
    
- [IEnumFBBlock](ienumfbblock.md) : cette interface prend en charge l'accès et l'énumération des blocs de données de disponibilité d'un utilisateur dans un intervalle de temps. 
    
   > [!NOTE]
   > Une énumération contient des blocs de disponibilité qui indiquent l'état de disponibilité des périodes sur le calendrier d'un utilisateur, dans un intervalle de temps (spécifié par [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)). Éléments d'un calendrier, tels que les rendez-vous et les demandes de réunion, les blocs de formulaire dans l'énumération. Les éléments adjacents les uns aux autres sur le calendrier et qui ont le même état de disponibilité sont combinés pour former un seul bloc. Une période de temps libre sur un calendrier forme également un bloc. Par conséquent, deux blocs consécutifs dans une énumération ne peuvent pas avoir le même état de disponibilité. Ces blocs ne se chevauchent pas dans le temps. Lorsqu'il y a des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour créer des blocs de disponibilité qui ne se chevauchent pas dans l'énumération en fonction de cet ordre de priorité: absent (e) du bureau, occupé (e). 
  
Pour enregistrer le fournisseur de disponibilité auprès d'Outlook, le fournisseur de messagerie doit effectuer les opérations suivantes:
  
1. Inscrivez le fournisseur de disponibilité à l'aide de COM, en fournissant un CLSID qui permet d'accéder à l'implémentation du fournisseur de **IFreeBusySupport**. 
    
2. Indiquez à Outlook que le fournisseur de disponibilité existe en définissant la clé suivante (où `<xx.x>` correspond à la version d'Outlook) dans le registre système: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Par exemple, si le fournisseur de transport est SMTP, pour enregistrer le fournisseur avec Microsoft Outlook 2010, définissez la clé suivante sur les données dans le tableau suivant: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Nom |Type |Valeur |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID pour la mise en œuvre respective de IFreeBusySupport}  |
   
   Dans ce scénario, Outlook co-crée la classe COM et l'utilise pour récupérer des informations de disponibilité pour les utilisateurs de messagerie SMTP.
    
Pour prendre en charge un carnet d'adresses et un fournisseur de transport qui utilisent un type d'entrée d'adresse autre que SMTP, modifiez le *nom* en conséquence. 
  
> [!NOTE]
> Pendant l'installation, les fournisseurs de disponibilité doivent vérifier si un paramètre de Registre pour le même type d'entrée d'adresse existe déjà. Si c'est le cas, le fournisseur de disponibilité doit remplacer le fournisseur actuel pour ce type d'entrée d'adresse et effectuer la restauration auprès de ce fournisseur lors de la désinstallation. Toutefois, si un utilisateur a installé plus d'un fournisseur de disponibilité pour le même type d'entrée d'adresse, l'utilisateur doit désinstaller ces fournisseurs dans l'ordre inverse en tant qu'installation (c'est-à-dire, toujours désinstaller le dernier fournisseur). Dans le cas contraire, le registre peut pointer vers un fournisseur qui a déjà été désinstallé. 
  
## <a name="api-components"></a>Composants de l'API

L'API de disponibilité inclut les composants suivants:
  
### <a name="definitions"></a>Définitions

- [Constantes (API de disponibilité)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Types de données

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

