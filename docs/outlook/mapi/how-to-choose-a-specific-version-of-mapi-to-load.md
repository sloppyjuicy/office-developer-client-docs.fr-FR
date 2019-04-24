---
title: Sélection d’une version spécifique de MAPI à charger
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344519"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Sélection d’une version spécifique de MAPI à charger

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous établissez une liaison explicite avec une implémentation de MAPI, vous devez soigneusement sélectionner l'implémentation à charger. 
  
Il existe deux méthodes pour établir une liaison explicite avec une implémentation de MAPI. 
  
1. Vous pouvez charger la bibliothèque de stub MAPI et spécifier dans le registre une DLL personnalisée pour charger et distribuer les appels MAPI à.
    
2. Vous pouvez implémenter l'algorithme de recherche de client MAPI pour rechercher la version de MAPI utilisée par le client de messagerie par défaut et le charger.
    
Étant donné que vous pouvez modifier les [paramètres du Registre stub Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) pour indiquer à votre application d'utiliser n'importe quelle implémentation de MAPI, nous vous recommandons de diriger votre application afin qu'elle utilise une implémentation de MAPI que vous avez testée avec. Ce qui suit décrit les deux méthodes de liaison explicite. 
  
## <a name="reading-from-the-registry"></a>Lecture à partir du Registre

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Pour lire les informations d'implémentation MAPI à partir du Registre

1. Les clés de Registre qui indiquent une DLL personnalisée pour un client de messagerie se trouvent `HKLM\Software\Clients\Mail` sous la clé du client de messagerie. 
    
   Le tableau suivant décrit ces clés:
    
   |**Clé**|**Description**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Un ID de catégorie PublishComponent Windows Installer (GUID) qui identifie la DLL qui exporte les appels MAPI simples ou MAPI. Si cette clé est définie, elle est prioritaire sur la clé **DllPath** ou **DLLPathEx** .  <br/> |
   |MSIApplicationLCID  <br/> |Identificateur de paramètres régionaux (LCID) de votre application. La première valeur de chaîne identifie une sous-clé `HKLM\Software` et les valeurs de chaîne suivantes identifient les valeurs de Registre sous cette clé qui contiennent des informations de paramètres régionaux.  <br/> |
   |MSIOfficeLCID  <br/> |LCID pour Microsoft Office. La première valeur de chaîne identifie une sous-clé `HKLM\Software` et les valeurs de chaîne suivantes identifient les valeurs de Registre sous cette clé.  <br/> |
   
   Obtenez les informations de ces clés.
    
2. TransMettez les valeurs que vous avez obtenues de l'étape précédente à la fonction [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** est une fonction qui est exportée par la bibliothèque de stub MAPI mapistub. dll. Elle renvoie le chemin d'accès de la version personnalisée de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Pour charger l'implémentation de MAPI marquée comme valeur par défaut

1. Lisez la `HKLM\Software\Clients\Mail::(default)` valeur de registre. 
    
2. Recherchez les informations pour le client indiqué comme décrit précédemment.
    
> [!NOTE]
> Notez que le client de messagerie par défaut ne peut pas implémenter MAPI étendu. 
  
#### <a name="example"></a>Exemple

Pour charger MAPI tel qu'il est implémenté par Outlook, recherchez les clés `HKLM\Software\Clients\Mail\Microsoft Outlook` de Registre sous et transférez-les vers **FGetComponentPath**. **FGetComponentPath** renverra le chemin d'accès à l'implémentation d'Outlook de MAPI. 
  
Si les clés **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID** ne sont pas définies, vérifiez la valeur de Registre **DLLPathEx** . Si les clés sont définies, **FGetComponentPath** indique le chemin d'accès de l'implémentation MAPI du client. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implémentation de l'algorithme de recherche de client MAPI

Le tableau suivant répertorie les quatre fonctions de MFCMAPI utilisées pour rechercher le chemin d'accès à une implémentation personnalisée de MAPI:
  
|**Fonction**|**Description**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtient le chemin d'accès de la bibliothèque MAPI.  <br/> |
| `GetMailKey` <br/> |Obtient la clé de registre de messagerie MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtient l'identificateur Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtient le chemin d'accès au composant à l'aide de [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Étant donné que MFCMAPI charge l'implémentation par défaut de MAPI par défaut, si vous voulez utiliser une autre implémentation de MAPI, vous devez explicitement le lui indiquer. Cette opération est effectuée à l'aide de la routine **MAPI Session\Load** . 
  
### <a name="how-these-functions-work"></a>Fonctionnement de ces fonctions

1. Les appels `GetMAPIPath`MFCMAPI, en transMETTANT la valeur null pour le paramètre client, pour charger l'implémentation MAPI par défaut.
    
2.  `GetMAPIPath`appelle `GetMapiMsiIds` pour lire les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`appels `GetMailKey` permettant d'ouvrir la clé de Registre pour le client de messagerie par défaut. 
    
4.  `GetMapiMsiIds`utilise le handle de Registre renvoyé `GetMailKey` par pour rechercher les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.
    
5. Les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**sont renvoyées à `GetMAPIPath`.  `GetMAPIPath`Ensuite, transmettez `GetComponentPath`-les à.
    
6.  `GetComponentPath`charge la bibliothèque de stub MAPI, Mapi32. dll, à partir du répertoire système. 
    
7.  `GetComponentPath`récupère ensuite l'adresse de la fonction **FGetComponentPath** à partir de Mapi32. dll, en supposant que Mapi32. dll exporte **FGetComponentPath**.
    
8. Si l'obtention de l'adresse de **FGetComponentPath** à partir de Mapi32 `GetComponentPath` . dll échoue, récupère l'adresse à partir de mapistub. dll. 
    
9.  `GetComponentPath`appelle ensuite **FGetComponentPath**, en obtenant le chemin d'accès de la version par défaut de MAPI.
    
10.  `GetMAPIPath`renvoie ensuite ce chemin d'accès à l'appelant, qui charge ensuite MAPI et y liens explicitement, comme décrit dans la rubrique [lien vers les fonctions MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Pour prendre en charge les copies localisées de MAPI pour l'anglais et les paramètres `GetMAPIPath` régionaux non anglais, lit les valeurs des sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** .  `GetMAPIPath`appelle ensuite **FGetComponentPath**, en spécifiant d'abord **MSIApplicationLCID** en tant que **szQualifier**et en spécifiant de nouveau **MSIOfficeLCID** en tant que **szQualifier**. Pour plus d'informations sur les clés de Registre pour les clients de messagerie qui prennent en charge les langues autres que l'anglais, consultez [la rubrique Setting up the MSI Keys for your MAPI dll](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Si MFCMAPI ne reçoit pas de chemin d'accès pour `GetMAPIPath`MAPI à l'aide de, il charge la bibliothèque de stubs MAPI à partir du répertoire système.
> - La valeur de Registre **MSMapiApps** abordée dans [mappage explicite des appels MAPI à des dll MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) s'applique uniquement lorsque la bibliothèque de stub MAPI est utilisée. Les applications qui chargent une implémentation spécifique de MAPI ou chargent l'implémentation par défaut n'ont pas besoin de définir la clé de Registre **MSMapiApps** . 
    
## <a name="see-also"></a>Voir aussi

- [FGetComponentPath](fgetcomponentpath.md)
- [Vue d’ensemble de la programmation MAPI](mapi-programming-overview.md)
- [Lien vers les fonctions MAPI](how-to-link-to-mapi-functions.md)
- [Paramètres de Registre stub Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Configuration des clés MSI pour votre DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Mappage explicite des appels MAPI aux dll MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

