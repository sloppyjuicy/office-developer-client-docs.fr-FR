---
title: À propos de l’API Disponibilité
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: L’API de libre/occupé permet aux fournisseurs de messagerie de fournir des informations d’état de libre/occupé pour les comptes d’utilisateur spécifiés dans un délai spécifié.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433758"
---
# <a name="about-the-freebusy-api"></a>À propos de l’API Disponibilité

L’API de libre/occupé permet aux fournisseurs de messagerie de fournir des informations d’état de libre/occupé pour les comptes d’utilisateur spécifiés dans un délai spécifié. L’état de libre/occupé d’un bloc de temps dans le calendrier d’un utilisateur est l’un des suivants : in-office, occupé, provisoire ou gratuit.
  
## <a name="create-a-freebusy-provider"></a>Créer un fournisseur de services de libre-service

Pour fournir des informations de libre/occupé aux utilisateurs de messagerie, un fournisseur de messagerie crée un fournisseur de libre/occupé et l’inscrit auprès d’Outlook. Le fournisseur de libre/occupé doit implémenter les interfaces suivantes. Notez qu’un certain nombre de membres dans ces interfaces ne sont pas pris en charge et doivent renvoyer les valeurs de retour spécifiées. En particulier, l’API de libre/occupé ne prend pas en charge l’accès en écriture aux informations de libre/occupé et déléguer l’accès aux comptes.
  
- [IFreeBusySupport](ifreebusysupport.md) : cette interface prend en charge la spécification des interfaces qui accèdent aux données de libre/occupé pour les utilisateurs spécifiés. Il utilise [FBUser pour](fbuser.md) identifier un utilisateur. 
    
- [IFreeBusyData](ifreebusydata.md) — Cette interface obtient et définit une plage de temps pour un utilisateur donné et renvoie une interface pour l’éumation des blocs de données de libre/occupé dans cette plage de temps. Il utilise le temps relatif pour obtenir et définir cette plage de temps. Pour plus d’informations, voir [Utiliser l’heure relative pour accéder aux données de libre/occupé.](how-to-use-relative-time-to-access-free-busy-data.md)
    
- [IEnumFBBlock —](ienumfbblock.md) Cette interface prend en charge l’accès et l’éumation des blocs de données de la période de libre/occupé d’un utilisateur. 
    
   > [!NOTE]
   > Une éumération contient des blocs de libre/occupé qui indiquent l’état de la période de libre/occupé du calendrier d’un utilisateur, dans une plage de temps (spécifiée par [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Éléments d’un calendrier, tels que les rendez-vous et les demandes de réunion, blocs de formulaire dans l’éumération. Les éléments qui sont adjacents les uns aux autres sur le calendrier et qui ont le même statut de libre/occupé sont combinés pour former un seul bloc. Une période gratuite sur un calendrier constitue également un bloc. Par conséquent, deux blocs consécutifs dans une éumération n’auraient pas le même statut de libre/occupé. Ces blocs ne se chevauchent pas dans le temps. Lorsqu’un calendrier se chevauche, Outlook fusionne ces éléments pour former des blocs de libre/occupé non superposés dans l’éumération en fonction de cet ordre de priorité : absence du bureau, occupé, provisoire. 
  
Pour inscrire le fournisseur de libre/occupé auprès d’Outlook, le fournisseur de messagerie doit :
  
1. Inscrivez le fournisseur de libre/occupé auprès de COM, en fournissant un CLSID qui permet d’accéder à l’implémentation du fournisseur **de IFreeBusySupport**. 
    
2. Faites savoir à Outlook que le fournisseur de services de libre-service existe en fixant la clé suivante (où représente la version d’Outlook) dans le Registre `<xx.x>` système : 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Par exemple, si le fournisseur de transport est SMTP, pour enregistrer le fournisseur auprès de Microsoft Outlook 2010, définissez la clé suivante sur les données du tableau suivant : 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Nom |Type |Valeur |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID pour l’implémentation respective d’IFreeBusySupport}  |
   
   Dans ce scénario, Outlook co-crée la classe COM et l’utilise pour récupérer des informations de libre/occupé pour tous les utilisateurs de messagerie SMTP.
    
Pour prendre en charge un carnet d’adresses et un fournisseur de transport qui utilisent un type d’entrée d’adresse autre que SMTP, modifiez  *le* nom en conséquence. 
  
> [!NOTE]
> Pendant l’installation, les fournisseurs de services de libre-service doivent vérifier si un paramètre de Registre pour le même type d’entrée d’adresse existe déjà. Si c’est le cas, le fournisseur de libre/occupé doit le faire pour ce type d’entrée d’adresse et le restaurer lors de sa désinstallation. Toutefois, si un utilisateur a installé plusieurs fournisseurs de libre/occupé pour le même type d’entrée d’adresse, il doit désinstaller ces fournisseurs dans l’ordre inverse en tant qu’installation (autrement dit, désinstaller toujours le dernier fournisseur). Sinon, le Registre peut pointer vers un fournisseur qui a déjà été désinstallé. 
  
## <a name="api-components"></a>Composants d’API

L’API de libre/occupé inclut les composants suivants :
  
### <a name="definitions"></a>Définitions

- [Constantes (API de libre/occupé)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Types de données

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

