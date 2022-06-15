---
title: Liste de vérification d’installation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Cette rubrique décrit les conditions préalables à l’installation d’un fournisseur Outlook Social Connector (OSC), et l’installation vérifie que le programme d’installation de votre fournisseur doit se terminer pour fonctionner correctement.
ms.openlocfilehash: a05a173cabbf2c15c9bc325b5e68ba73cc1b07cd
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66084031"
---
# <a name="installation-checklist"></a>Liste de vérification d’installation

Cette rubrique décrit les conditions préalables à l’installation d’un fournisseur Outlook Social Connector (OSC), et l’installation vérifie que le programme d’installation de votre fournisseur doit se terminer pour fonctionner correctement.
  
## <a name="installation-overview"></a>Vue d’ensemble de l’installation

Les utilisateurs doivent installer les fournisseurs OSC uniquement si une version prise en charge de Outlook est présente et que le système d’exploitation est installé et activé sur l’ordinateur client. Les versions de Outlook prises en charge sont Office Outlook 2003, Office Outlook 2007, Outlook 2010 et Outlook 2013 (installées sur l’ordinateur client ou, dans le cas de Outlook 2010 et Outlook  2013, remis par Démarrer en un clic sur l’ordinateur client). Pour garantir la réussite de l’installation, le programme d’installation de votre fournisseur doit effectuer les opérations suivantes :
  
- Vérifiez si une version prise en charge de Outlook est présente.

- Vérifiez si le système d’exploitation est installé.

> [!NOTE]
> Click-to-Run est un environnement virtuel dans lequel Outlook 2010 (32 bits) ou Outlook 2013 (32 bits) peuvent s’exécuter. Pour Outlook 2013, vérifiez si la clé VirtualOutlook existe dans HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook du registre Windows. Pour plus d’informations sur la distribution de Outlook en tant que produit démarrer en un clic sur un ordinateur client, consultez [Comment vérifier si Outlook est disponible sur un ordinateur en tant que produit démarrer en un clic](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx).
  
Toutefois, l’utilisateur doit s’assurer que le système d’exploitation est activé avant d’installer le fournisseur.
  
Les tiers, y compris les fournisseurs OSC, ne peuvent pas redistribuer la osc. Toutefois, si le système d’exploitation n’est pas installé, le programme d’installation du fournisseur peut utiliser les liens g appropriés pour installer le système d’exploitation sur l’ordinateur client. Un lien g est une URL spécialement construite sur <https://g.live.com> laquelle un utilisateur est transféré vers une page web correspondante pour télécharger l’OSC. Un lien G OSC est mis en forme en tant que <https://g.live.com/0CR> lien _Glink_ _LCID_/ , où _LCID_ et _Glink_ spécifient les paramètres régionaux, la version et le bitness de Outlook sur l’ordinateur client. Chaque lien g pointe vers un exécutable et est spécifique aux valeurs  _LCID_ et  _Glink_ spécifiées.
  
Par exemple, le lien g pour installer la dernière version de l’OSC pour Outlook 2003 ou Outlook 2007 pour le LCID 1033 (anglais des États-Unis) est le suivant :
  
<https://g.live.com/0CR1033/80>
  
Pour plus d’informations sur les valeurs _Glink_ pour les différentes versions et le nombre de bits de Outlook, ainsi que sur les valeurs _LCID_ pour les paramètres régionaux pris en charge, consultez la section 7 de la liste de [vérification de l’installation](#olosc_InstallationOverview_InstallationChecklist) ci-dessous.

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Liste de vérification d’installation

Le package d’installation du fournisseur doit effectuer une série de vérifications d’installation, comme illustré dans la figure 1, pour vérifier que le fournisseur s’installe correctement.
  
**Figure 1. Logique d’installation du fournisseur**

![Liste de vérification d’installation](media/odc_ol14_ta_OSC_Fig07.gif)
  
La procédure suivante décrit les vérifications d’installation décrites dans la figure 1.
  
1. Comme prérequis, déterminez si Outlook est installé ou présent, et s’il est installé ou présent, déterminez si la version de Outlook prend en charge le système d’exploitation. Pour plus d’informations sur la détection de la version installée de Outlook, consultez [Vérifier la version de Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).

   - Si la version installée de Outlook est antérieure à Outlook 2003, la procédure d’installation du fournisseur ne peut pas se terminer. Indiquez à l’utilisateur d’obtenir une version prise en charge de Outlook et de la osc avant de procéder à l’installation du fournisseur OSC.

   - Si Outlook n’est pas installé, passez à l’étape 2.

   - Si Outlook 2003 ou Outlook 2007 est installé, passez à l’étape 3.

   - Si Outlook 2010 ou Outlook 2013 est installé, passez à l’étape 4.

2. **Procédez comme suit si Outlook n’est pas installé sur l’ordinateur client :**

   1. Vérifiez si le système d’exploitation est installé en tant que composant par défaut d’une installation démarrer en un clic de Outlook 2010 ou Outlook 2013. Examinez la `VirtualOutlook` clé à l’emplacement suivant dans le registre Windows :

      - Pour Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`

      - Pour Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`

      La `VirtualOutlook` clé est une valeur REG_SZ qui contient la balise locale, telle que « en-us », du produit installé.

   2. Si la `VirtualOutlook` clé n’existe pas, Outlook n’est pas présente sur l’ordinateur client et la procédure d’installation du fournisseur ne peut pas se terminer. Indiquez à l’utilisateur d’obtenir une version prise en charge de Outlook et de la osc avant de procéder à l’installation du fournisseur OSC.

   3. Si la `VirtualOutlook` clé existe, Outlook a été remis par Démarrer en un clic sur l’ordinateur client. Passez à la vérification de la version installée de la bibliothèque de types OSC en examinant la `OSCVersion` clé à l’emplacement suivant dans le registre Windows :

      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`

      La valeur est `OSCVersion` une chaîne qui spécifie le numéro de version de la bibliothèque de types de Socialprovider.dll (par exemple, « 1.0 », « 1.1 » ou « 15 »).

   4. S’il `OSCVersion` s’agit de « 1.0 », « 1.1 » ou « 15 », une version appropriée d’OSC est installée. Passez à l’étape 6 pour rechercher les paramètres régionaux de l’interface utilisateur Outlook actuels afin de préparer l’installation de la dernière version de l’OSC.

   5. Sinon, `OSCVersion` ne contient pas de valeur attendue. Passez à l’étape 6 pour rechercher les paramètres régionaux de l’interface utilisateur Outlook actuels afin de préparer l’installation d’une version appropriée de l’OSC.

3. **Passez à cette étape si Outlook 2003 ou Outlook 2007 est installé sur l’ordinateur client :**

   1. Vérifiez si le système d’exploitation est installé en écrivant une action personnalisée de programme d’installation pour tester l’existence de l’ID de composant qualifié suivant :

      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`

      L’ID de composant qualifié est un GUID qui fournit une méthode d’indirection de niveau unique, similaire à un pointeur. Pour plus d’informations sur Windows Programme d’installation, consultez [la feuille de route pour Windows documentation du programme d’installation](/windows/win32/msi/roadmap-to-windows-installer-documentation).

   2. Si le composant qualifié spécifié existe, une version du système d’exploitation est installée. Passez à l’étape 5 pour rechercher les paramètres régionaux de l’interface utilisateur Outlook actuels afin de préparer l’installation de la dernière version de l’OSC.

   3. Sinon, le système d’exploitation n’est pas installé. Passez à l’étape 6 pour rechercher les paramètres régionaux de l’interface utilisateur Outlook actuels afin de préparer l’installation d’une version appropriée de l’OSC.

4. **Passez à cette étape si Outlook 2010 ou Outlook 2013 est installé sur l’ordinateur client :**

   1. Déterminez le bitness de la version installée de Outlook en examinant la `Bitness` clé à l’emplacement suivant dans le registre Windows :

      - Pour Outlook 2010, examinez`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`

      - Pour Outlook 2013, examinez`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`

      La `Bitness` clé est « x86 » pour les Outlook 32 bits, ou « x64 » pour les Outlook 64 bits.

   2. Si votre fournisseur est un fournisseur managé et que vous avez compilé le composant fournisseur spécifiant la plateforme cible en tant **qu’UC,** passez à l’étape 6 pour rechercher les paramètres régionaux de l’interface utilisateur Outlook actuels pour préparer l’installation de la dernière version de l’OSC. Votre fournisseur fonctionne sur les versions 32 bits et 64 bits de l’OSC.

   3. Si votre fournisseur est un composant COM natif, examinez le nombre de bits de la version installée de Outlook :

      - Si la version installée de Outlook est 32 bits, votre procédure d’installation devra installer un fournisseur 32 bits (à l’étape 8), après avoir vérifié qu’un osc approprié est installé.

      - Sinon, la version installée de Outlook est 64 bits, et votre procédure d’installation devra installer un fournisseur 64 bits (à l’étape 8), après avoir vérifié qu’un osc approprié est installé.

   4. Passez à l’étape 6 pour rechercher les paramètres régionaux de l’interface utilisateur Outlook actuels afin de préparer l’installation d’une version appropriée de l’OSC.

5. **Passez à cette étape si Outlook 2003 ou Outlook 2007 est installé et que le système d’exploitation est installé sur l’ordinateur client :** vérifiez les paramètres régionaux actuels de l’interface utilisateur Outlook en examinant la `OSCLcid` clé à l’emplacement suivant dans le registre Windows :

   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`

   La `OSCLcid` clé est une valeur DWORD qui spécifie les balises de paramètres régionaux IETF (Internet Engineering Task Force) (définies par [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), qui représentent les paramètres régionaux d’interface utilisateur Outlook actuels. Passez à l’étape 7 pour installer la dernière osc sur l’ordinateur client.

6. **Passez à cette étape si Outlook 2003 ou Outlook 2007 est installé, ou si Outlook 2010 ou Outlook 2013 est présent, mais que la dernière version d’OSC n’est pas nécessairement installée sur l’ordinateur client :**

   Utilisez l’objet **LanguageSettings** pour déterminer le LCID des paramètres régionaux de l’interface utilisateur Outlook. L’extrait de code Visual Basic Scripting Edition (VBScript) suivant montre comment obtenir le LCID des paramètres régionaux de l’interface utilisateur Outlook.

   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. **Passez à cette étape si le programme d’installation a le LCID de la version installée de Outlook, mais que la dernière version d’OSC n’est pas nécessairement installée sur l’ordinateur client :**

   Chaînez un lien g dans votre package d’installation pour vous assurer que la dernière version de l’OSC est installée sur l’ordinateur client. Le format de lien g est le suivant :

   <https://g.live.com/0CR>_LCID_/  _Glink_

   Reportez-vous au tableau 1 ci-dessous pour les valeurs  _LCID_ prises en charge et au tableau 2 pour les valeurs  _Glink_ prises en charge. Par exemple, le lien g pour installer la dernière version de l’OSC 32 bits pour 32 bits Outlook Social Connector 2013 (anglais des États-Unis) est le suivant :

   <https://g.live.com/0CR1033/82>

8. Installez le fournisseur. La procédure d’installation du fournisseur doit inscrire l’identificateur de programme (ProgID) à l’emplacement de registre Windows approprié. Pour plus d’informations, consultez [Inscription d’un fournisseur](registering-a-provider.md). Assurez-vous également que le nombre de bits du fournisseur à installer est identique à celui de la version de Outlook présente sur l’ordinateur client. Par exemple, installez un fournisseur 32 bits si 32 bits Outlook 2013 est présent, et un fournisseur 64 bits si Outlook 2013 est installé. Pour Outlook 2003 ou 2007, seule la version 32 bits de votre fournisseur s’applique.

**Tableau 1 : Paramètres régionaux pris en charge et valeurs LCID correspondantes en hexadécimal pour l’OSC**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|fr  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kz-kz  <br/> |1087  <br/> |
|ko-kr  <br/> |1042  <br/> |
|lt-lt  <br/> |1063  <br/> |
|lv-lv  <br/> |1062  <br/> |
|nb-no  <br/> |1044  <br/> |
|nl-nl  <br/> |1043  <br/> |
|pl-pl  <br/> |1045  <br/> |
|pt-br  <br/> |1046  <br/> |
|pt-pt  <br/> |2070  <br/> |
|ro-ro  <br/> |1048  <br/> |
|ru-ru  <br/> |1049  <br/> |
|sk-sk  <br/> |1051  <br/> |
|sl-si  <br/> |1060  <br/> |
|sr-cyrl-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |

**Tableau 2 : Valeurs Glink prises en charge pour osc**
  
|**Valeur Glink**|**Fonction**|
|:-----|:-----|
|80  <br/> |Installe la dernière version d’OSC pour Outlook 2003 ou Outlook 2007. |
|82  <br/> |Installe le dernier correctif d’OSC 32 bits pour Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013. |
|83  <br/> |Installe le dernier correctif d’OSC 64 bits pour Outlook 2010 ou Outlook Social Connector 2013. |

## <a name="see-also"></a>Voir aussi

- [Inscription d’un fournisseur](registering-a-provider.md)
- [Étapes rapides pour Learning développer un fournisseur](quick-steps-for-learning-to-develop-a-provider.md)
- [Déploiement d'un fournisseur](deploying-a-provider.md)
