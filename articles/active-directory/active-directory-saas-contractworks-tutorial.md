---
title: 'チュートリアル: Azure Active Directory と ContractWorks の統合 | Microsoft Docs'
description: Azure Active Directory と ContractWorks の間でシングル サインオンを構成する方法について説明します。
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.reviewer: joflore
ms.assetid: e7b269d6-3c4e-4bc4-a55f-5071d1f52591
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 04/16/2018
ms.author: jeedes
ms.openlocfilehash: 3c986810f3d994b956d4c81fd80b38d9dfee4f50
ms.sourcegitcommit: 59914a06e1f337399e4db3c6f3bc15c573079832
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2018
---
# <a name="tutorial-azure-active-directory-integration-with-contractworks"></a>チュートリアル: Azure Active Directory と ContractWorks の統合

このチュートリアルでは、ContractWorks と Azure Active Directory (Azure AD) を統合する方法について説明します。

ContractWorks と Azure AD の統合には、次の利点があります。

- ContractWorks にアクセスする Azure AD ユーザーを制御できます。
- ユーザーが自分の Azure AD アカウントで自動的に ContractWorks にサインオン (シングル サインオン) できるようにします。
- 1 つの中央サイト (Azure Portal) でアカウントを管理できます。

SaaS アプリと Azure AD の統合の詳細については、「[Azure Active Directory のアプリケーション アクセスとシングル サインオンとは](active-directory-appssoaccess-whatis.md)」をご覧ください。

## <a name="prerequisites"></a>前提条件

ContractWorks と Azure AD の統合を構成するには、次のものが必要です。

- Azure AD サブスクリプション
- ContractWorks でのシングル サインオンが有効なサブスクリプション

> [!NOTE]
> このチュートリアルの手順をテストする場合、運用環境を使用しないことをお勧めします。

このチュートリアルの手順をテストするには、次の推奨事項に従ってください。

- 必要な場合を除き、運用環境は使用しないでください。
- Azure AD の評価環境がない場合は、[1 か月の評価版を入手できます](https://azure.microsoft.com/pricing/free-trial/)。

## <a name="scenario-description"></a>シナリオの説明
このチュートリアルでは、テスト環境で Azure AD のシングル サインオンをテストします。 このチュートリアルで説明するシナリオは、主に次の 2 つの要素で構成されています。

1. ギャラリーからの ContractWorks の追加
2. Azure AD シングル サインオンの構成とテスト

## <a name="adding-contractworks-from-the-gallery"></a>ギャラリーからの ContractWorks の追加
Azure AD への ContractWorks の統合を構成するには、ギャラリーから管理対象 SaaS アプリの一覧に ContractWorks を追加する必要があります。

**ギャラリーから ContractWorks を追加するには、次の手順に従います。**

1. **[Azure Portal](https://portal.azure.com)** の左側のナビゲーション ウィンドウで、**[Azure Active Directory]** アイコンをクリックします。 

    ![Azure Active Directory のボタン][1]

2. **[エンタープライズ アプリケーション]** に移動します。 次に、**[すべてのアプリケーション]** に移動します。

    ![[エンタープライズ アプリケーション] ブレード][2]
    
3. 新しいアプリケーションを追加するには、ダイアログの上部にある **[新しいアプリケーション]** をクリックします。

    ![[新しいアプリケーション] ボタン][3]

4. 検索ボックスに「**ContractWorks**」と入力し、結果パネルで **[ContractWorks]** を選び、**[追加]** をクリックして、アプリケーションを追加します。

    ![結果リストの ContractWorks](./media/active-directory-saas-contractworks-tutorial/tutorial_contractworks_addfromgallery.png)

## <a name="configure-and-test-azure-ad-single-sign-on"></a>Azure AD シングル サインオンの構成とテスト

このセクションでは、"Britta Simon" というテスト ユーザーに基づいて、ContractWorks で Azure AD のシングル サインオンを構成し、テストします。

シングル サインオンを機能させるには、Azure AD ユーザーに対応する ContractWorks ユーザーが Azure AD で認識されている必要があります。 言い換えると、Azure AD ユーザーと ContractWorks の関連ユーザーの間で、リンク関係が確立されている必要があります。

ContractWorks で Azure AD のシングル サインオンを構成してテストするには、次の構成要素を完了する必要があります。

1. **[Azure AD シングル サインオンの構成](#configure-azure-ad-single-sign-on)** - ユーザーがこの機能を使用できるようにします。
2. **[Azure AD のテスト ユーザーの作成](#create-an-azure-ad-test-user)** - Britta Simon で Azure AD のシングル サインオンをテストします。
3. **[ContractWorks テスト ユーザーの作成](#create-a-contractworks-test-user)** - ContractWorks で Britta Simon に対応するユーザーを作成し、Azure AD の Britta Simon にリンクさせます。
4. **[Azure AD テスト ユーザーの割り当て](#assign-the-azure-ad-test-user)** - Britta Simon が Azure AD シングル サインオンを使用できるようにします。
5. **[シングル サインオンのテスト](#test-single-sign-on)** - 構成が機能するかどうかを確認します。

### <a name="configure-azure-ad-single-sign-on"></a>Azure AD シングル サインオンの構成

このセクションでは、Azure Portal で Azure AD のシングル サインオンを有効にして、ContractWorks アプリケーションでシングル サインオンを構成します。

**ContractWorks で Azure AD シングル サインオンを構成するには、次の手順に従います。**

1. Azure Portal の **ContractWorks** アプリケーション統合ページで、**[シングル サインオン]** をクリックします。

    ![シングル サインオン構成のリンク][4]

2. **[シングル サインオン]** ダイアログで、**[モード]** として **[SAML ベースのサインオン]** を選択し、シングル サインオンを有効にします。

    ![[シングル サインオン] ダイアログ ボックス](./media/active-directory-saas-contractworks-tutorial/tutorial_contractworks_samlbase.png)

3. **[ContractWorks のドメインと URL]** セクションで、**IDP** 開始モードでアプリケーションを構成する場合は、次の手順に従います。

    ![[ContractWorks のドメインと URL] のシングル サインオン情報](./media/active-directory-saas-contractworks-tutorial/tutorial_contractworks_url.png)

    **[識別子]** ボックスに次の URL を入力します。`https://login.securedocs.com/saml/metadata`

4. アプリケーションを **SP** 開始モードで構成する場合は、**[詳細な URL 設定の表示]** チェックボックスをオンにして次の手順を実行します。

    ![[ContractWorks のドメインと URL] のシングル サインオン情報](./media/active-directory-saas-contractworks-tutorial/tutorial_contractworks_url1.png)

    **[サインオン URL]** ボックスに、「`https://login.securedocs.com/saml/hint`」と入力します。
     
5. ContractWorks アプリケーションは、特定の形式で構成された SAML アサーションを受け入れます。 このアプリケーションには、次の要求を構成します。 これらの属性の値は、アプリケーション統合ページの **[ユーザー属性]** セクションで管理できます。 次のスクリーンショットはその例です。
    
    ![[Configure Single Sign-On]](./media/active-directory-saas-contractworks-tutorial/tutorial_ContractWorks_attribute.png)

6. **[シングル サインオン]** ダイアログの **[ユーザー属性]** セクションで、上の図に示すように SAML トークン属性を構成し、次の手順を実行します。
    
    | 属性名 | 属性値 |
    | ---------------| --------------- |
    | mail | User.mail |
    | displayName | user.displayname |

    a.[サインオン URL] ボックスに、次のパターンを使用して、ユーザーが RightScale アプリケーションへのサインオンに使用する URL を入力します。 **[属性の追加]** をクリックして **[属性の追加]** ダイアログを開きます。

    ![[Configure Single Sign-On]](./media/active-directory-saas-contractworks-tutorial/tutorial_attribute_04.png)

    ![[Configure Single Sign-On]](./media/active-directory-saas-contractworks-tutorial/tutorial_attribute_05.png)
    
    b. **[名前]** ボックスに、その行に対して表示される属性名を入力します。
    
    c. **[値]** 一覧から、その行に対して表示される値を入力します。

    d. **[名前空間]** は空白のままにします。
    
    d. **[OK]** をクリックします。

7. **[SAML 署名証明書]** セクションで、コピー ボタンをクリックして **[App Federation Metadata Url]\(アプリケーション フェデレーション メタデータ URL\)** をコピーし、メモ帳に貼り付けます。
    
    ![[Configure Single Sign-On]](./media/active-directory-saas-contractworks-tutorial/tutorial_metadataurl.png)
     
8. **[保存]** ボタンをクリックします。

    ![[シングル サインオンの構成] の [保存] ボタン](./media/active-directory-saas-contractworks-tutorial/tutorial_general_400.png)

9. **ContractWorks** 側でシングル サインオンを構成するには、生成された**アプリケーション フェデレーション メタデータ URL** を [ContractWorks サポート チーム](mailto:support@contractworks.com)に送信する必要があります。 サポート チームはこれを設定して、SAML SSO 接続が両方の側で正しく設定されるようにします。

### <a name="create-an-azure-ad-test-user"></a>Azure AD のテスト ユーザーの作成

このセクションの目的は、Azure Portal で Britta Simon というテスト ユーザーを作成することです。

   ![Azure AD のテスト ユーザーの作成][100]

**Azure AD でテスト ユーザーを作成するには、次の手順に従います。**

1. Azure Portal の左側のウィンドウで、**Azure Active Directory** のボタンをクリックします。

    ![Azure Active Directory のボタン](./media/active-directory-saas-contractworks-tutorial/create_aaduser_01.png)

2. ユーザーの一覧を表示するには、**[ユーザーとグループ]** に移動し、**[すべてのユーザー]** をクリックします。

    ![[ユーザーとグループ] と [すべてのユーザー] リンク](./media/active-directory-saas-contractworks-tutorial/create_aaduser_02.png)

3. **[ユーザー]** ダイアログ ボックスを開くには、**[すべてのユーザー]** ダイアログ ボックスの上部にある **[追加]** をクリックしてきます。

    ![[追加] ボタン](./media/active-directory-saas-contractworks-tutorial/create_aaduser_03.png)

4. **[ユーザー]** ダイアログ ボックスで、次の手順に従います。

    ![[ユーザー] ダイアログ ボックス](./media/active-directory-saas-contractworks-tutorial/create_aaduser_04.png)

    a. **[名前]** ボックスに「**BrittaSimon**」と入力します。

    b. **[ユーザー名]** ボックスに、ユーザーである Britta Simon の電子メール アドレスを入力します。

    c. **[パスワードを表示]** チェック ボックスをオンにし、**[パスワード]** ボックスに表示された値を書き留めます。

    d. **Create** をクリックしてください。
 
### <a name="create-a-contractworks-test-user"></a>ContractWorks テスト ユーザーの作成

このセクションでは、ContractWorks で Britta Simon というユーザーを作成します。 [ContractWorks サポート チーム](mailto:support@contractworks.com)と連携し、ContractWorks プラットフォームにユーザーを追加します。 シングル サインオンを使用する前に、ユーザーを作成し、有効化する必要があります。 

### <a name="assign-the-azure-ad-test-user"></a>Azure AD テスト ユーザーの割り当て

このセクションでは、Britta Simon に ContractWorks へのアクセスを許可することで、このユーザーが Azure シングル サインオンを使用できるようにします。

![ユーザー ロールを割り当てる][200] 

**ContractWorks に Britta Simon を割り当てるには、次の手順に従います。**

1. Azure Portal でアプリケーション ビューを開き、ディレクトリ ビューに移動します。次に、**[エンタープライズ アプリケーション]** に移動し、**[すべてのアプリケーション]** をクリックします。

    ![ユーザーの割り当て][201] 

2. アプリケーションの一覧で **[ContractWorks]** を選択します。

    ![アプリケーションの一覧の ContractWorks のリンク](./media/active-directory-saas-contractworks-tutorial/tutorial_contractworks_app.png)  

3. 左側のメニューで **[ユーザーとグループ]** をクリックします。

    ![[ユーザーとグループ] リンク][202]

4. **[追加]** ボタンをクリックします。 次に、**[割り当ての追加]** ダイアログで **[ユーザーとグループ]** を選択します。

    ![[割り当ての追加] ウィンドウ][203]

5. **[ユーザーとグループ]** ダイアログで、ユーザーの一覧から **[Britta Simon]** を選択します。

6. **[ユーザーとグループ]** ダイアログで **[選択]** をクリックします。

7. **[割り当ての追加]** ダイアログで **[割り当て]** ボタンをクリックします。
    
### <a name="test-single-sign-on"></a>シングル サインオンのテスト

このセクションでは、アクセス パネルを使用して Azure AD のシングル サインオン構成をテストします。

アクセス パネルで [ContractWorks] タイルをクリックすると、自動的に ContractWorks アプリケーションにサインオンします。
アクセス パネルの詳細については、[アクセス パネルの概要](active-directory-saas-access-panel-introduction.md)に関する記事を参照してください。 

## <a name="additional-resources"></a>その他のリソース

* [SaaS アプリと Azure Active Directory を統合する方法に関するチュートリアルの一覧](active-directory-saas-tutorial-list.md)
* [Azure Active Directory のアプリケーション アクセスとシングル サインオンとは](active-directory-appssoaccess-whatis.md)



<!--Image references-->

[1]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_04.png

[100]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_201.png
[202]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_202.png
[203]: ./media/active-directory-saas-contractworks-tutorial/tutorial_general_203.png

