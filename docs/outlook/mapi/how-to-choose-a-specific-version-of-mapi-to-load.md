---
title: Sélection d’une version spécifique de MAPI à charger
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: Découvrez comment choisir une version spécifique de MAPI à charger.
ms.openlocfilehash: 34ebaaef7ffafc3e8d0a04190bb867004209bcf5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375929"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Sélection d’une version spécifique de MAPI à charger

**S’applique à** : Outlook 2013 | Outlook 2016
  
Lorsque vous liez explicitement une implémentation de MAPI, vous devez soigneusement sélectionner l’implémentation à charger.
  
Il existe deux méthodes pour établir un lien explicite avec une implémentation de MAPI.
  
1. Chargez la bibliothèque stub MAPI et spécifiez dans le Registre une DLL personnalisée pour charger et envoyer des appels MAPI. Ou,

2. Implémentez l’algorithme de recherche du client MAPI pour rechercher la version de MAPI utilisée par le client de messagerie par défaut et la charger.

Étant donné que vous pouvez modifier l’Paramètres de Registre [ stubMapi32.dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) pour que votre application utilise n’importe quelle implémentation de MAPI, nous vous recommandons d’orienter votre application vers une implémentation de MAPI que vous avez testée. Les deux méthodes de liaison sont explicitement décrits ci-après.
  
## <a name="read-mapi-implementation-information-from-the-registry"></a>Lire les informations d’implémentation MAPI à partir du Registre

1. Les clés de Registre qui indiquent une DLL personnalisée pour un client de messagerie `HKLM\Software\Clients\Mail` se trouvent sous la clé du client de messagerie.

   Le tableau suivant décrit les clés suivantes :

   |**Clé**|**Description**|
   |:-----|:-----|
   | MSIComponentID <br/> |Un Windows ID de catégorie (GUID) PublishComponent du programme d’installation qui identifie la DLL qui exporte des appels MAPI ou MAPI simples. Si elle est définie, cette clé est prioritaire sur la **touche DLLPath** ou **DLLPathEx** . |
   | MSIApplicationLCID <br/> |Identificateur de paramètres régionaux (LCID) pour votre application. La première valeur de chaîne identifie une sous-clé `HKLM\Software` à partir de et les valeurs de chaîne suivantes identifient les valeurs de Registre sous cette clé qui contiennent des informations de paramètres régionaux. |
   | MSIOfficeLCID  <br/> |LCID pour Microsoft Office. La première valeur de chaîne identifie une sous-clé `HKLM\Software` à partir de et les valeurs de chaîne suivantes identifient les valeurs de Registre sous cette clé. |

   Obtenez les informations à partir de ces clés.

2. Passez les valeurs obtenues à l’étape précédente à la [fonction FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** est une fonction exportée par la bibliothèque stub MAPI Mapistub.dll. Elle renvoie le chemin d’accès de la version personnalisée de MAPI.

## <a name="loading-the-implementation-of-mapi-marked-as-default"></a>Chargement de l’implémentation de MAPI marqué comme valeur par défaut

1. Lisez la `HKLM\Software\Clients\Mail::(default)` valeur de Registre.

2. Recherchez les informations pour le client indiqué comme décrit précédemment.

> [!NOTE]
> Notez que le client de messagerie par défaut peut ne pas implémenter MAPI étendu.
  
### <a name="example"></a>Exemple

Pour charger MAPI tel qu’implémenté par Outlook, `HKLM\Software\Clients\Mail\Microsoft Outlook` recherchez les clés de Registre sous et passez-les à **FGetComponentPath**. **FGetComponentPath** retourne le chemin d’Outlook’implémentation de MAPI.
  
Si les clés **MSIComponentID**, **MSIApplicationLCID** et **MSIOfficeLCID** ne sont pas définies, vérifiez la valeur de Registre **DLLPathEx** . Si les clés sont définies, **FGetComponentPath** indique le chemin d’accès de l’implémentation de MAPI du client.
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implémentation de l’algorithme de recherche de client MAPI

Le tableau suivant répertorie les quatre fonctions MFCMAPI utilisées pour rechercher le chemin d’accès à une implémentation personnalisée de MAPI :
  
|**Fonction**|**Description**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtient le chemin d’accès de la bibliothèque MAPI. |
| `GetMailKey` <br/> |Obtient la clé de Registre de messagerie MAPI. |
| `GetMapiMsiIds` <br/> |Obtient l’Windows du programme d’installation. |
| `GetComponentPath` <br/> |Obtient le chemin d’accès du [composant à l’aide de FGetComponentPath](fgetcomponentpath.md). |

Étant donné que MFCMAPI charge l’implémentation par défaut de MAPI par défaut, si vous souhaitez utiliser une implémentation différente de MAPI, vous devez explicitement lui en faire part. Cette opération est effectuée à l’aide de la routine **Session\Load MAPI** .
  
### <a name="how-these-functions-work"></a>Fonctionnement de ces fonctions

1. Appels MFCMAPI `GetMAPIPath`, en passant NULL pour le paramètre client, pour charger l’implémentation MAPI par défaut.

2. `GetMAPIPath` pour `GetMapiMsiIds` lire les **valeurs de MSIComponentID**, **MSIApplicationLCID** et **MSIOfficeLCID**.

3. `GetMapiMsiIds` pour `GetMailKey` ouvrir la clé de Registre pour le client de messagerie par défaut.

4. `GetMapiMsiIds` utilise le handle de `GetMailKey` Registre renvoyé par pour rechercher des **valeurs pour MSIComponentID**, **MSIApplicationLCID** et **MSIOfficeLCID**.

5. Les **valeurs de MSIComponentID**, **MSIApplicationLCID** et **MSIOfficeLCID** sont renvoyées à `GetMAPIPath`. `GetMAPIPath` puis les transmet à `GetComponentPath`.

6. `GetComponentPath` charge la bibliothèque stub MAPI, Mapi32.dll, à partir du répertoire système.

7. `GetComponentPath` extrait ensuite l’adresse de la **fonction FGetComponentPath** à partir Mapi32.dll, en supposant que Mapi32.dll exporte **FGetComponentPath**.

8. Si l’obtention de l’adresse **de FGetComponentPath** à partir Mapi32.dll échoue, `GetComponentPath` extrait l’adresse de Mapistub.dll.

9. `GetComponentPath` appelle ensuite **FGetComponentPath**, en obtenant le chemin d’accès de la version par défaut de MAPI.

10. `GetMAPIPath` renvoie ensuite ce chemin d’accès à l’appelant, qui charge ensuite MAPI et y lie explicitement, comme décrit dans l’lien [vers les fonctions MAPI](how-to-link-to-mapi-functions.md).

> [!NOTE]
>
> - Pour prendre en charge les copies localisées de MAPI pour les paramètres régionaux anglais et non anglais, `GetMAPIPath` lit les valeurs des sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** . `GetMAPIPath` appelle ensuite **FGetComponentPath**, en spécifiant **d’abord MSIApplicationLCID** en **tant que szQualifier**, puis en spécifiant **MSIOfficeLCID** en tant que **szQualifier**. Pour plus d’informations sur les clés de Registre pour les clients de messagerie qui ne sont pas en anglais, voir [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).
> - Si MFCMAPI ne reçoit pas de chemin d’accès pour MAPI à `GetMAPIPath`l’aide, il charge la bibliothèque stub MAPI à partir du répertoire système.
> - La valeur de Registre **MSMapiApps** abordée dans Mappage explicite des appels [MAPI aux DLL MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) s’applique uniquement lorsque la bibliothèque Stub MAPI est utilisée. Les applications qui chargent une implémentation spécifique de MAPI ou chargent l’implémentation par défaut n’ont pas besoin de définir la clé de Registre **MSMapiApps** .

## <a name="see-also"></a>Voir aussi

- [FGetComponentPath](fgetcomponentpath.md)
- [Vue d’ensemble de la programmation MAPI](mapi-programming-overview.md)
- [Lien vers les fonctions MAPI](how-to-link-to-mapi-functions.md)
- [Mapi32.dll registre Stub Paramètres](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Configuration des clés MSI pour votre DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Mappage explicite des appels MAPI aux DLL MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)
