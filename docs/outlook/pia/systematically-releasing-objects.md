---
title: Lancement systématique des objets
TOCTitle: Systematically releasing objects
ms:assetid: d4cd1d8e-aae6-483b-a4d8-1656171e838d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623945(v=office.15)
ms:contentKeyID: 55119785
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 812f720b3ebab1100040802d7593548063497297
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406833"
---
# <a name="systematically-releasing-objects"></a>Lancement systématique des objets

Cette rubrique fait la synthèse des recommandations sur l'arrêt des compléments pour les développeurs de compléments et les administrateurs qui utilisent Outlook. Pour plus d’informations, voir[arrêt des modifications pour Outlook 2010](https://msdn.microsoft.com/library/ee720183\(v=office.15\)).

## <a name="add-in-shutdown-changes-in-outlook"></a>L’application shutdown change dans Outlook

En commençant dans Outlook 2010, Outlook, par défaut, ne signale pas de compléments qu’il arrête. Plus précisément, Outlook n'appelle plus les méthodes** OnBeginShutdown(Matrice)** et**OnDisconnectionn(ext\_DisconnectMode, Matrice)** méthodes de l'interface**IDTExtensibility2**lors des arrêts rapides. De façon similaire, un complément Outlook écrit avec des outils de développement Microsoft Office dans Microsoft Visual Studio 2010 ou une version plus récente, n'appelle plus la méthode ThisAddin\_Shutdown lorsqu’Outlook s'arrête. 

La raison pour laquelle ces méthodes ne sont plus appelées est que, alors qu'une majorité de compléments effectuent des tâches simples telles que libérer des références, certains compléments effectuent des appels de services Web ou d'autres opérations de longue durée en même temps que ces événements, ce qui retarde l'arrêt d'Outlook de façon significative. Suite à cette modification, Outlook fonctionne mieux que dans le passé lorsque vous l’arrêtez.

## <a name="recommendations-for-add-in-shutdown-for-developers"></a>Recommandations pour les développeurs relatives à l'arrêt des compléments

Il est important que les développeurs respectent les recommandations suivantes pour l'arrêt des compléments de façon à garantir que les utilisateurs finals continuent de bénéficier d'un arrêt d'Outlook rapide et réactif.

- Les compléments doivent continuer d'implémenter les méthodes OnBeginShutdown et OnDisconnection ou ThisAddin\_Shutdown pour libérer des références et de la mémoire allouée, car il existe des scénarios dans lesquels les administrateurs souhaitent revenir à un arrêt lent via la stratégie de groupe ou dans lesquels l'utilisateur peut déconnecter manuellement votre complément via la boîte de dialogue **Compléments COM**.

- Les développeurs de complément doivent seulement effectuer des tâches qui doivent absolument avoir lieu pendant l’arrêt.

- Les développeurs de compléments doivent évaluer les performances de leurs compléments dans différents scénarios et selon différents paramètres du Registre Windows contrôlant l'arrêt d'Outlook, et modifier leurs compléments de façon pro-active pour qu'ils fonctionnent avec Outlook.

## <a name="recommendations-for-add-in-shutdown-for-it-administrators"></a>Recommandations pour les administrateurs relatives à l'arrêt des compléments

Pour les administrateurs, s'il existe des compléments déjà déployés dans une entreprise et qu'ils ne peuvent pas être mis à niveau pour devenir compatibles avec le nouveau mécanisme d'arrêt d'Outlook, ils peuvent recourir à quelques nouveaux paramètres du Registre Windows pour revenir au comportement d'arrêt lent.

### <a name="individual-add-in-setting"></a>Paramétrage d'un complément individuel

Les administrateurs peuvent permettre des notifications d'arrêt à des compléments Outlook dans le cadre d'un déploiement de compléments. Bien que vous ne puissiez pas faire cela via une stratégie de groupe, c'est pratique si vous avez des conditions requises en matière de compatibilité descendante pour des compléments spécifiques.

Configurez ce paramètre pour chaque complément via l'inscription du complément dans les ruches du Registre HKCU ou HKLM, en ajoutant une valeur supplémentaire à l'inscription du complément. Entrez le texte suivant sur une seule ligne :

`HKCU\Software\Microsoft\Office\Outlook\Add-ins\<ProgID>[RequireShutdownNotification]=dword:0x1`

Paramétrer cette valeur 0x1permet au complément de recevoir des rappels bloqués pendant la fermeture d’Outlook. Ceci a un impact sur les performances de l'arrêt d'Outlook et doit être évalué dans le cadre d'un déploiement. Ce paramètre doit être utilisé uniquement si un complément possède de problèmes de compatibilité significatifs avec le nouveau mécanisme d’arrêt. Le paramétrage de la valeur à 0x0 utilise le comportement par défaut d'Outlook.

### <a name="global-setting"></a>Paramètre global

Les administrateurs informatiques peuvent globalement activer les notifications d’arrêt pour tous les compléments via une stratégie de groupe. Ceci est recommandé pour les organisations qui ont un grand nombre de solutions internes ou d'ordinateurs où ce paramétrage doit être déployé pour assurer la compatibilité lors d'une mise en œuvre d'Outlook.

Utilisez ce paramétrage pour modifier le nouveau mécanisme d'arrêt de façon à ce qu'il corresponde à celui utilisé par Outlook 2007. Vous pouvez déployer le paramétrage de stratégie de groupe, par utilisateur ou par ordinateur. Tapez le texte suivant en une seule ligne :

`HKCU\Policies\Microsoft\Office\Outlook\15.0\Options\Shutdown[AddinFastShutdownBehavior]=dword:0x1`

Le paramétrage de AddinFastShutdownBehavior à 0x1 permet les notifications d'arrêt pour tous les compléments. Le paramétrage de la valeur à 0x0 utilise le comportement par défaut d'Outlook.

