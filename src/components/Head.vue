<template>
    <header class="header">
        <a class="logo"
           href="https://m.huya.com"
           :style="{ backgroundImage: `url('${logoBase64}')`}"
        >
        </a>
        <a class="header-search"
            href="">
            <span class="header-search-icon"
                  :style="{  backgroundImage:
                  `url('${searchIconBase64}')`}"
            ></span>
        </a>
        <a class="header-app" href="">打开App</a>
    </header>
</template>

<script lang="ts">
import {Component, Prop, Vue} from 'vue-property-decorator'

@Component
export default class Head extends Vue {
    @Prop({
        type: String,
        default: "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMgAAAA8CAMAAAAUhQWjAAAABGdBTUEAALGPC/xhBQAAAwBQTFRFg4OD5Y4U8pwQpo15aGhot1oftlkfm5ubuV0eZ2dnZ2dnw2cc24IYxmwb2Ika230Y9J8Q3YUVy3AaaWlpmZmZznIaZmZmnJycu14fnZ2dvGEdyG8cwmYdyGwcxWob03kYy3AbmZmZwWQdul8e9aAPym8a9KAPZ2dn9qERtVkftVgfym8daWlpmpqa9aAPZmZm9aAPm5ubmZmZZ2dnn5+f9aAP9aER8ZsRmpqamZmZ0nMdvmIdsVQhul4e3H4d9qERc3NzZmZmZ2dnm5ubZmZmnJycZ2dnnp6e9aAQ9aAQ8pwQmpqa4ooY9aAPZmZmZ2dn9Z8Qy3Ac9KAPmpqa9aAQ9qEQ9qAQ7pMX7pYV96EQ9aAQ9J4PZmZmZ2dndXV1aWlpZmZmmZmZmpqampqaa2traWlpmpqarE8iZ2dnZmZmmpqatFcf8JwRmZmZmpqaZmZmZ2dnZmZmmZmZmZmZmpqampqampqaqamp4IgUZmZmZmZmZ2dnmpqampqaZmZmZ2dnZmZmZ2dnmpqaaWlpmpqampqaZ2dnaGhop0kjm5ubmZmZ1HsXZmZmmpqam5ubampqmZmZZ2dnZmZmaGhoZ2dnZ2dnZmZmmpqasJlympqaZ2dnn5+fqkwirlEhZ2dnZ2dnZ2dnm5ubZ2dnZ2dnZ2dnZmZmZmZmZ2dnaGhoZ2dngICA75kQmpqaZmZmampqZ2dnmpqaaGhoaGhompqar6mca2trZmZmZmZmmZmZ9J8PZmZmAAAA48Gw1ZZiypF71KeT2JxqyX5FtGRFz5yI3LWm9OfizpmExIVsvGMk16yauW1NvWcvy4JJ5byY4rSKy5R+v3le3KZ4qU0o8di/+OnczYVO/Pj07NjP8+Tar1o4/vz60ItT4L6wqlAtv2sy4K2B6cWkuGErtVsmwnE40pBa7tG1xnc+9uTT134Xt1se+u/msFQi+vPv3YQV6JES5Y0Tul4dyW4a2YEVxGobtVkfvWEdzHIZ65UR0HYYsVQgwWYc44sT850PpkgjmZmZ////G+OeoQAAALx0Uk5TGIf3IJvutWPjnpyvK5AnK13yyCfeqZMo4TSXUr6i+Oh/7Mrt3OTrmm/y9VwjS+b1zza3/RP7Zafq6yvY+eYTRgr8WmGgQ4EX8rCIVh/26YWbY3Vvj31SDhc+4MLKvQYf4vjRRyovjP5n+/7/MRmTxKR9Z6h4mSML/8/vSsuf4DTmUoAWiMCqG/9P1v+HkC0Q01YodnHzrOUI8LIc//9e22NdeUPXitL4Nk0F/6m2DCyuPFGSAiaW65b//wCko3TUAAALKklEQVRo3t2ad1wUZxrH88f1fsnlUi/JpZyxYtdYwd5BBMWooDGAESKgRCmCBDBiNkgMi0HcRXHpiEqT3Z3PXdpdosYSNRoVD6VLrwssMOy9Zco7szO7q+jnA/f7Y/dtO/t+532e93nfd+YJ6v9ET5CZNWvkmo38xfPLhhDIszEzZr440rzRC8Npozpm+rShArKSNhpaOoze00Usr7zUmKPrazOq/jZEQH5uzNEB5QR1v/EKyGb7rp7svMRliRMq1en6FKpfLRsKICvpIB2rnHUu65brxOpqGTFtCIA826Ozqu4ZvoMeZJqqyTqIrm2Em7VLui9IS0vTDKRThcfBFfLNy5VpaY5R5q2jPDXuBMhvbRgQoMaZhVa68a4eaP1BXhjq+Bl5ZQmvEAWv4GfeY1hMNI0rykte4L/eDpSGEiDDm81coq2zx0etUvu09HT39nFj8qotIALZw2IHvbySQC/9czltgGUhfD5XSVGeSbm5CAQ39EvfmEFcIJ4HmeYjpMhR1KorSu5W1dTUVF288lWZquU+w6JY+YAg77nD4gQLIB+B22uhWr+BorYwyaxEqQY/40F+3y0YjB7v6ou3TYQa7pZ6t3ahypcTrYNsKOKFzTqqyFzhsOmcoiIwZO5WQPNZkGyyoUNCRGqCPjctjwd5NYcYjVZ1ZYPJTDUl6k40Kkuk+n8qk9EcZOGZAu3JRogwRbrYUdg0j/EAd04eyMv4PBrRbHd77COF/nq90t0dOdKHwOYy9MFxxKz1Bs/RW3/hR5OkaqqNMNZMmm3OMUpvUXM4m8uSAQGXYAcqExYHM5mnntondHb3FXq93bvYFj+k7FPBuOwhQP7McSjq75lkda8emuDyteYDYhkkGc6eKLVPDkQj91vsY/ysdaoYYLozIH/V6yfMIeKIG2dZ7WU1Jgv6sawVmNciX0mQ4GNAaM45dEwoMPhUEqxIpeRA8mXvwkkSJEqp9IduEwBz8xyhESqVGg5kNcvRWXqD7/VPl7+5I3aWGxUw4Lw9SwokCaaCBfZChIEQWHHGMoifKMIcNQMJlUL1Y0Hc/sFw3C8jOt5wi6bpq9/9JCS5XQqta12hJEhwBp7eMwhFIE+nkOVD97QEskVEf8g2kA0syGKGI6iedPM7NNYPQpS6cujxb0qChEj9jT0O7TA5Ic4yyKF4QllSICdDk0Esj8g6CHOOodCQF4QWMSCTGY4+H4Gf/4sBoWMu3yDLr9UDj1q+TAokMx91LiCfENNTFJiDqQfwkXApEKoQ2q6GnbWigOeHjGKc3W0RO2FVC279DzSnr2+SFSWt0LgkfSQKLUWOJQsUClv4oYVHwHFCxbBoGEhoJEHSpUHAhdIoFoTK0utXeDAgS9hAWC/orulrHoT+L2ledXBIdLOlQJL1csa1wMLsvJ4Fid9HyJ4AsddokHdk2QekOTg4BgR8gkJ+QEDARvDpiUDWcANSInTrWzRJ8h+iprJTPCQsyBnZSHAySR7Ez6qzH2OXKJIBKw2BuLJTb22VBRD632Q0MepEQ8KC2H8mISYIemhYxaO/T0DLJiXIe7AgIRGEkgiQLQKQ8PDwjfC7GCTsWJBEdurNKTdZALlKjoipHK4fF0v5iOMnYsWbhRRPNLkl5Flx9o0ESFT88eMcSALF+wiKswiEi4WKShHIebkBMZkutME1l5s5yIfykZnnQE6ekCkxawV/RChAytnlQZxYkNZLIhBi1oo5J6y61A5/4SwCOSTt7CIQDRqPkMyHC4jyIGNYEIPIRUzf8p5+R1RVZdAJ3f0U9jkKWf+WPayOmoMo0QR91FMyjgwjtsgHM+VA0MIB7UfA9wQGxJdb9nbUiXrLRnb6/E3x2vFaC/zFJP6MdQ8KHxQFF3QJ7lxxuhjE/td4qxRnQ0A8KgsiNWs5cyD14t42XMXDce62+XIeH1Ws5joITcrBgyqMgGtSShZEgzaFdsdsiuyyIBlgPY02BWdAIp0BcZIHMX0HMb6tk1jNf9mJfuLK9RDsC/T+uDd2HnIgcb/BUeOU7BIlLY+QxwP5yGIOxMesxw3fXL7TILktKetFP5nCneCEoG1bNlwHKSkRCAMWtwDFjfRQrnbjAzn7ScsgYzmQnnsmW3W3Ax+pjGX/ELiGQyhe4aaRHUHR/L2EELCYikeTVXgys/7PS09HA8Jg5qYjqoh0oTB6ejyVF5wOrVbviUxLqVTijRVIpDIgY/g97nWbOVTNQeoYldHwMtvhVH0xvDvz9BkBgjuaz291QUft/EOz2Zot/FEP1ASLO+VDbPP1hbLOPok/PKmvswmjrlLVqNN1+QAHUrHdyjqDDn1G+X8mso0564uBVgD7yc9NJqev0BWwInwYs0EJLrYkR0oDm4fPi6L2pUooGYAs4kD6OqttwKi6rvJBDpLTAeLkIDrExqYV1N3j09bXUmFpTG5cu/TPCjXdwR45AhLvQQQCnL25VQ3MBOzE+3rUldeEG/SbVRfvfll5oeL7cnUMreroUXQRB3nGGYMIZEqvAYW9dnzYbqDrv6++XlJy/avq0rJy7xjoCOoOQ3tr9/2gLvExd9NrgwjkabwKqWWP27saO3sMLbUthh7Y+cbmrj4LDxmmDCKQlXh126SzWTn8MTF/lLJrW1hYCk6u0moDKSpFq/XCc+04rVa7k1pYoNXOxxE6WqudC74PaFl5jSb7tDSWq4DNxkWzucgD+OoibdueCEGyoX/Q3bYxtMP5qs+oNrThceIPHA/09/fvxcnDIElRu8HnTpSPBqnt1H7wGYbyR0DqU/Ad2M8rmucII4pBs5StfHYTAP6831y70ROr6YCjg7zh8hyd9H10yg08R62A543UQEDG7TiBdHpTf//WheSFDp9gtIqi3gKVp2F6PKj4GIPA/G623V9AYi4EgbbFPc9talc3oYdVEhhBPrQ3pmyHg9jRpHMZEAinE6BgPmdYIKPl697H3YeCSNkIZBdzFVSRAhKx6PDhNdrADkY7M3sp6I5e0QQFpuiYL6oxSBPyK1XjsgGBTJwbifUpKNjMXgj3ixNs/A5OQoREDuR9EmQbAhkZwwxIrxF0DwN0gKBR29rW29zbG9TY3V6roulbXzSYShmsFkQynRKCTN2BtMk2kJ0Ca38UINSTzAE2DBpqJn3l3Pmr/JZdbegsh08bzrJPRGGh9+9EIIRsANkBe7IXauqjAlnzOoqFkINmHlLnVIBu36zoVnQr2hqboUF1nb1y+14na4OwreDVFAjy+QdINo7Ix+ALu/iORwVC+S4Hrow4aAW7OQEDcLeV9JK+7rNlXLSppemZlBjkwXwEzjYTSZCUwMClAwSh1i7KUWMjYn28udp0xewVgmZiIh4xyzrIMyjvhebH0VIjMpGYtQrB51tms9ZCuVlLGoTyfYnxBi6KtJZaCpKNw0UvCpmBfABv5WkomH+OOgIC2yaUH49BYPd3owIcRyDI35k4cpoRWCEAB9o6Hqb34p9ZAaFemIGnVN6Smi2F+CniR29mIEemEr4fxgwMGbKfOUzkIykWBN0Buci+2ToI9YeZEMRo21LF1WzRlhjp5bWfWWsVFATCMLEqtgCLqdgcjbNhTBw5EsjUF0SjcBgYG7sKfu+PZssL4OrtuUg2h9Za22NjA9GKLTI2Fi3ujnjFxo4TvHj2vDdYBNuCMXb2gBaqZpH9kb/TOOtFVYt1jLf/9ND/tmv0fiC4WBz/WEEo6o9Pv24Nwznx4f8thbP2pY8ZBM7ETovkKVwG9gLd/MNY7/ySevwgwG/XOi8eYw6x2HXtUHnvl5Tb2tWT33R1cXJyWeLqPHm175rB/f6yPMhQ0/8A4LB+1+zdxwgAAAAASUVORK5CYII="
    })
    logoBase64!: string
    
    @Prop({
        type: String,
        default: "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAMAAACelLz8AAAABGdBTUEAALGPC/xhBQAAAMxQTFRFmpqal5eXmZmZl5eXmpqamJiYmZmZmJiYnp6eoaGh////mpqal5eXmJiYl5eXl5eXmJiYmpqal5eXmJiYmZmZl5eXmZmZl5eXmJiYl5eXl5eXmJiYmJiYnJycmpqamZmZl5eXmJiYmJiYmJiYmJiYl5eXmpqamJiYm5ubmJiYmJiYmJiYmZmZmJiYl5eXmJiYmJiYm5ubl5eXv7+/oqKimJiYnp6eoqKil5eXmJiYmpqal5eXmJiYqqqqmJiYqqqqnJycmJiYAAAAl5eX9hENsQAAAEN0Uk5TU9E37l1egJ8iEwEr3dKl5z5EO2hVh5OsxKKzhnwsYmsgisj5w/Y1simSv0Vfz8D30C67BBbtFQv9V0z44QPUCR/8ADikRfcAAAEcSURBVCjPddLXlsIgEAbg7LrF3nt37W3VGDcxpvK//zs5kHBSjjs3QD4CA4PCZORzhazLYqGErVm+gaI0mKZo9QMZ860ep8ODf8w4RdGevYgONF7ORtRzzR31LU3SiuYePbnD5wlY2CHRPkc9SmzvA+OATFrNiyc9pCVtQWVgFhfmVoAqpzydZ5Qg1gZanHLALSmsCXQ4FQAnRXWgyykLFFNUA1ROLvBwk9QAeiLDEmAmqQ9MBA2AXUI2dGZP0HQOfMTk+gusw4vaAqd9JN+AcQlJPwP+MExlQ//AuMuieBYNK+1mvdbo+6Ke/l2WUlsgCuPLCSx4APbYkrK+sL/A5LOxq61OV+1NRHmEKQp7Fdys18S0N6j/ELPfr0+9a56Zwk818QAAAABJRU5ErkJggg=="
    })
    searchIconBase64!: string
}
</script>

<style lang="stylus" scoped>
    .header
        position relative

        width 100%
        height 54px
        border-bottom 1px solid #EDEDED
        box-sizing border-box
        .logo
            position absolute
            top 50%
            left 0
            transform translateY(-50%)

            margin-left 7.5px
            width 100px
            height 30px

            background-size 100% 100%
        .header-search
            display flex
            justify-content center
            align-items center
            position absolute
            top 50%
            right 104.75px
            transform translateY(-50%)

            width 42px
            height 28px
            border-radius 14px

            background #F4F4F4
            .header-search-icon
                width 16px
                height 16px

                background-size 100% 100%
        .header-app
            position absolute
            top 50%
            right 7.5px
            transform translateY(-50%)

            width 86px
            height 28px
            border-radius 15px

            background: #FFA200
            color #fff
            text-align center
            line-height 28px
            text-decoration-line none
            font-size 13px
            font-weight 345
</style>